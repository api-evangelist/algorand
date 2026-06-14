# Algorand GraphQL Schema

## Overview

This GraphQL schema provides a unified interface over the Algorand Algod and Indexer REST APIs. The Algorand blockchain exposes two core REST daemons: **Algod** for real-time node interaction (submitting transactions, querying account balances, retrieving blocks, managing smart contracts) and the **Indexer** for deep historical querying of accounts, assets, applications, transactions, and blocks from a PostgreSQL-backed store.

The schema consolidates both APIs into a single, strongly-typed GraphQL surface organized around the core Algorand primitives: nodes, blocks, transactions, accounts, assets, and applications.

## Source APIs

- **Algod REST API** — https://dev.algorand.co/reference/rest-api/algod/
- **Indexer REST API** — https://dev.algorand.co/reference/rest-api/indexer/
- **OpenAPI (Algod)** — https://raw.githubusercontent.com/algorand/go-algorand/master/daemon/algod/api/algod.oas3.yml
- **OpenAPI (Indexer)** — https://raw.githubusercontent.com/algorand/indexer/main/api/indexer.oas3.yml

## Schema File

See `algorand-schema.graphql` in this directory for the full type definitions.

## Type Summary

| Category | Types |
|---|---|
| Node / Health | `Node`, `NodeStatus`, `NodeVersion`, `Token`, `APIKey` |
| Blocks | `Block`, `BlockDetails`, `BlockHeader`, `BlockHash`, `Round`, `MiniBlock` |
| Transactions | `Transaction`, `TransactionDetails`, `TransactionType`, `SignedTransaction`, `UnsignedTransaction`, `InnerTransaction`, `PendingTransaction`, `StateProof` |
| Transaction Kinds | `PaymentTransaction`, `KeyRegTransaction`, `AssetConfigTransaction`, `AssetTransferTransaction`, `AssetFreezeTransaction`, `ApplicationCallTransaction` |
| Accounts | `Account`, `AccountDetails`, `AccountAsset`, `AccountAssetInfo`, `AccountParticipation`, `AccountStatus` |
| Assets | `Asset`, `AssetDetails`, `AssetParams`, `AssetFrozen` |
| Applications | `Application`, `ApplicationDetails`, `ApplicationParams`, `ApplicationLocalState`, `GlobalState`, `LocalState`, `StateSchema` |
| Signing | `LogicSig`, `MultiSig` |
| Ledger | `Microalgos`, `Balance`, `Supply`, `SupplyDetails` |
| Infrastructure | `Pool`, `Websocket` |

## Key Queries

```graphql
# Get node health and status
query {
  node {
    status { lastRound catchupTime hasSyncedSinceStartup }
    version { major minor patch }
  }
}

# Fetch a block by round
query {
  block(round: 45000000) {
    round
    timestamp
    transactions { id type }
    header { previousBlockHash genesisId rewardsLevel }
  }
}

# Look up an account
query {
  account(address: "ABC123...") {
    amount
    status
    assets { assetId amount isFrozen }
    participation { voteFirstValid voteLastValid voteKeyDilution }
  }
}

# Search transactions
query {
  transactions(address: "ABC123...", limit: 20, afterRound: 40000000) {
    id
    type
    confirmedRound
    payment { amount receiver }
    assetTransfer { assetId amount receiver }
  }
}

# Query asset details
query {
  asset(id: 31566704) {
    index
    params { name unitName total decimals clawback freeze manager reserve }
    destroyed
  }
}

# Query application (smart contract) state
query {
  application(id: 1002541853) {
    id
    params { approvalProgram clearStateProgram globalStateSchema localStateSchema }
    globalState { key value { type bytes uint } }
  }
}
```

## Mutations

```graphql
# Submit a signed transaction
mutation {
  submitTransaction(signedTxn: "<base64-encoded-msgpack>") {
    txId
  }
}

# Compile TEAL source
mutation {
  compileTeal(source: "#pragma version 9\nint 1") {
    result
    hash
  }
}
```

## Authentication

Algorand nodes use an `X-Algo-API-Token` header for authentication. Public archival nodes provided by Nodely (`mainnet-api.4160.nodely.dev`) and the legacy AlgoNode endpoints are freely accessible on the free tier without a token.

In a GraphQL gateway implementation, this token is passed via HTTP headers:

```
X-Algo-API-Token: <your-token>
```

## Pagination

The Indexer API uses cursor-based pagination via a `next-token` field returned in list responses. In this GraphQL schema, pagination is modeled with `nextToken` on list result types, which maps directly to the Indexer's cursor mechanism.

## Notes

- All amounts are expressed in **microalgos** (`Microalgos` scalar, 1 ALGO = 1,000,000 microalgos).
- Round numbers are used as the canonical reference for blockchain height (no concept of "block number" separate from round).
- The `StateProof` type supports cross-chain verification and light-client use cases.
- Inner transactions (from AVM smart contract execution) are nested under `TransactionDetails.innerTransactions`.
