# Algorand

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Algorand is a pure proof-of-stake blockchain platform designed for speed, security, and decentralization. It exposes REST APIs through two core daemons — Algod (the Algorand protocol daemon) for real-time node interaction including submitting transactions, querying account balances, retrieving blocks, and managing smart contracts; and the Indexer daemon for deep historical querying of accounts, assets, applications, transactions, and blocks from a PostgreSQL-backed store. A third daemon, KMD (Key Management Daemon), handles local key storage and signing. Public archival endpoints are freely available via third-party providers such as Nodely/AlgoNode, and the developer toolchain is anchored by AlgoKit with SDKs for Python, JavaScript, Go, and Java.

**Areas:** Blockchain · Cryptocurrency · Proof of Stake · DeFi · Smart Contracts

## Algorand on APIs.io

Everything profiled for Algorand is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/algorand/](https://apis.io/providers/algorand/)** — or go straight to one of the APIs or properties below.

### APIs (15)

- [Algorand KMD REST API](https://apis.io/apis/algorand/algorand-kmd-api/) — The Key Management Daemon (KMD) REST API provides local key storage and transaction signing for Algorand nodes. It exposes wallet management, key…
- [Algorand Common API](https://apis.io/apis/algorand/algorand-common-api/) — The common API from Algorand — 6 operation(s) for common.
- [Algorand Key API](https://apis.io/apis/algorand/algorand-key-api/) — The Key API from Algorand — 4 operation(s) for key.
- [Algorand Lookup API](https://apis.io/apis/algorand/algorand-lookup-api/) — The lookup API from Algorand — 14 operation(s) for lookup.
- [Algorand Master Key API](https://apis.io/apis/algorand/algorand-master-key-api/) — The Master Key API from Algorand — 1 operation(s) for master key.
- [Algorand Multisig API](https://apis.io/apis/algorand/algorand-multisig-api/) — The Multisig API from Algorand — 6 operation(s) for multisig.
- [Algorand Private API](https://apis.io/apis/algorand/algorand-private-api/) — The private API from Algorand — 7 operation(s) for private.
- [Algorand Program API](https://apis.io/apis/algorand/algorand-program-api/) — The Program API from Algorand — 1 operation(s) for program.
- [Algorand Public API](https://apis.io/apis/algorand/algorand-public-api/) — The public API from Algorand — 43 operation(s) for public.
- [Algorand Search API](https://apis.io/apis/algorand/algorand-search-api/) — The search API from Algorand — 6 operation(s) for search.
- [Algorand Swagger.json API](https://apis.io/apis/algorand/algorand-swagger-json-api/) — The Swagger.json API from Algorand — 1 operation(s) for swagger.json.
- [Algorand Transaction API](https://apis.io/apis/algorand/algorand-transaction-api/) — The Transaction API from Algorand — 1 operation(s) for transaction.
- [Algorand Versions API](https://apis.io/apis/algorand/algorand-versions-api/) — The Versions API from Algorand — 1 operation(s) for versions.
- [Algorand Wallet API](https://apis.io/apis/algorand/algorand-wallet-api/) — The Wallet API from Algorand — 6 operation(s) for wallet.
- [Algorand Wallets API](https://apis.io/apis/algorand/algorand-wallets-api/) — The Wallets API from Algorand — 1 operation(s) for wallets.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### GraphQL (1)

GraphQL schemas.

- [Algorand GraphQL Schema](https://apis.io/graphqls/algorand/algorand-graphql/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Algorand Agentic Access](https://apis.io/agentic-access/algorand/algorand-agentic-access/)

#### JSON Schema (3)

The data models the API reads and writes.

- [Algod REST API.](https://apis.io/schemas/algorand/algorand-algod/)
- [Indexer](https://apis.io/schemas/algorand/algorand-indexer/)
- [for KMD HTTP API](https://apis.io/schemas/algorand/algorand-kmd/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Algorand Context](https://apis.io/jsonld/algorand/algorand-context/)

#### Examples (2)

Example requests and responses.

- [Algorand Algod Examples](https://apis.io/examples/algorand/algorand-algod-examples/)
- [Algorand Indexer Examples](https://apis.io/examples/algorand/algorand-indexer-examples/)

#### Collections (36)

Postman and Open Collection request collections.

- [Algod REST API. common API](https://apis.io/collections/algorand/open-algorand-common-api/)
- [Algod REST API. common data API](https://apis.io/collections/algorand/open-algorand-data-api/)
- [Algod REST API. common experimental API](https://apis.io/collections/algorand/open-algorand-experimental-api/)
- [Algod REST API. common Key API](https://apis.io/collections/algorand/open-algorand-key-api/)
- [Algod REST API. common lookup API](https://apis.io/collections/algorand/open-algorand-lookup-api/)
- [Algod REST API. common Master Key API](https://apis.io/collections/algorand/open-algorand-master-key-api/)
- [Algod REST API. common Multisig API](https://apis.io/collections/algorand/open-algorand-multisig-api/)
- [Algod REST API. common nonparticipating API](https://apis.io/collections/algorand/open-algorand-nonparticipating-api/)
- [Algod REST API. common participating API](https://apis.io/collections/algorand/open-algorand-participating-api/)
- [Algod REST API. common private API](https://apis.io/collections/algorand/open-algorand-private-api/)
- [Algod REST API. common Program API](https://apis.io/collections/algorand/open-algorand-program-api/)
- [Algod REST API. common public API](https://apis.io/collections/algorand/open-algorand-public-api/)
- [Algod REST API. common search API](https://apis.io/collections/algorand/open-algorand-search-api/)
- [Algod REST API. common Swagger.json API](https://apis.io/collections/algorand/open-algorand-swagger-json-api/)
- [Algod REST API. common Transaction API](https://apis.io/collections/algorand/open-algorand-transaction-api/)
- [Algod REST API. common Versions API](https://apis.io/collections/algorand/open-algorand-versions-api/)
- [Algod REST API. common Wallet API](https://apis.io/collections/algorand/open-algorand-wallet-api/)
- [Algod REST API. common Wallets API](https://apis.io/collections/algorand/open-algorand-wallets-api/)
- [Algod REST API. common API](https://apis.io/collections/algorand/postman-algorand-common-api/)
- [Algod REST API. common data API](https://apis.io/collections/algorand/postman-algorand-data-api/)
- [Algod REST API. common experimental API](https://apis.io/collections/algorand/postman-algorand-experimental-api/)
- [Algod REST API. common Key API](https://apis.io/collections/algorand/postman-algorand-key-api/)
- [Algod REST API. common lookup API](https://apis.io/collections/algorand/postman-algorand-lookup-api/)
- [Algod REST API. common Master Key API](https://apis.io/collections/algorand/postman-algorand-master-key-api/)
- [Algod REST API. common Multisig API](https://apis.io/collections/algorand/postman-algorand-multisig-api/)
- …and 11 more published on APIs.io

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Algorand — jsonschema rules](https://apis.io/rules/algorand/algorand-jsonschema-spectral-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Algorand Authentication](https://apis.io/security/algorand/algorand-authentication/)
- [Algorand Domain Security](https://apis.io/security/algorand/algorand-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Algorand Plans](https://apis.io/plans/algorand/algorand-plans/)

#### Rate limits (1)

Published request limits.

- [Algorand Rate Limits](https://apis.io/rate-limits/algorand/algorand-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Algorand Finops](https://apis.io/finops/algorand/algorand-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://algorand.co/)
- [Documentation](https://dev.algorand.co/reference/rest-api/overview/)
- [Getting started](https://dev.algorand.co/getting-started/portal-guide/)
- [Support](https://dev.algorand.co/)
- [Blog](https://algorand.co/blog)
- [Terms of service](https://algorand.co/terms)
- [Privacy policy](https://algorand.co/privacy-policy)
- [GitHub](https://github.com/algorand)

## API Evangelist rating

**Kin Score 39.2** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 62.5 |
| Contract quality | 46.5 |
| Contract governance | 9.8 |
| Operational transparency | 10.5 |
| Developer ergonomics | 75.0 |
| Access clarity | 18.4 |

**Agent readiness 23.7** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 20.6** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/algorand/](https://apis.io/providers/algorand/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Algorand: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/algorand/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
