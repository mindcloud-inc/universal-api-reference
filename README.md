# Universal API Reference

![Last sync](https://img.shields.io/github/last-commit/mindcloud-inc/universal-api-reference?label=last%20sync)

The API surface of **3,192 apps** — **75,506 endpoints** — documented in one uniform, greppable format. Every app gets the same treatment: authentication, pagination, filtering, sorting, argument conventions, response formats, and a mapping back to the vendor's native API. One file per endpoint.

```bash
git clone https://github.com/mindcloud-inc/universal-api-reference.git

# every app that can issue a refund
rg -l "refund" apis

# how a specific API paginates, straight from the spec
rg "pagination" apis/s/stripe/universal-api/README.md -A 3
```

## Why this exists

APIs are filthy things. If there is one true REST standard, precious few companies have ever fully followed it. Every vendor invents its own pagination, its own filtering syntax, its own creative interpretation of HTTP status codes. This repo documents all of them the same way, so you don't have to be a specialist in a system to consume its API:

- Request & response formats and datatypes
- Pagination
- Filtering & sorting
- HTTP methods & status codes
- Native-API mapping (endpoint, quirks, source docs)

Averaged out, that's ~23.7 documented endpoints per app — most integration platforms cover 7–8.

## What's in this repo

- `apis/<letter>/<api>/universal-api/` — the Universal API README, auth, pagination, filtering, sorting, argument conventions, examples, and one file per action.
- `apis/<letter>/<api>/native-api/` — the vendor-native API README and one file per native operation.
- [`catalog.json`](catalog.json) — machine-readable catalog of all 3,192 apps, with per-letter shards under [`catalog/`](catalog).
- [`indexes/`](indexes) — app indexes by category, API specification, and native-docs link.
- [`llms.txt`](llms.txt) — index of this repo for LLM ingestion.
- [`indexes/api-specifications.md`](indexes/api-specifications.md) — generated Universal API OpenAPI files and provider-published Native API specifications.
- [`indexes/native-api-docs.md`](indexes/native-api-docs.md) — the vendors' own API documentation, one link per app.

### Example: one endpoint file

#### [Stripe: Cancel Payment Intent](apis/s/stripe/universal-api/actions/cancel-payment-intent.md)

Cancels an existing payment intent in Stripe.

```http
PUT https://connect.mindcloud.co/v1/universal/stripe/latest/actions/cancel-payment-intent
```

Native API mapping: `POST payment_intents/:intent/cancel` — [vendor documentation](https://docs.stripe.com/api/payment_intents/cancel).

## Where these docs come from

This is not scraped documentation. It's a nightly mirror of the machine-readable spec that drives [MindCloud](https://mindcloud.co)'s integration gateway — the product of years of building and validating app integrations, and the same spec its production systems execute API calls against at a [run rate of ~1.85 billion per year](https://mindcloud.co/api-calls). When a doc is wrong, real workflows break, and the spec gets fixed. Changes land here as daily commits, so you can watch it evolve in the history.

Full disclosure: MindCloud sells a [Universal API and MCP](https://mindcloud.co/docs/universal/rest/home/latest) that can call every endpoint in this repo through one interface.

## Ways to use it

- **Native API reference** — integrating directly with an app? Each endpoint file documents the native endpoint, arguments, pagination, and quirks, with links to source docs. No account, no SDK, no gateway required.
- **Agent context** — point your agent or RAG pipeline at [`llms.txt`](llms.txt) and `catalog.json`, or vendor the folders for the apps you care about.
- **Grep across every API at once** — find every app with a `refund` endpoint, every API that paginates by cursor, every endpoint that touches `invoice`.
- **Unified API / MCP** — if you'd rather call all 3,192 apps through one REST signature and auth model, that's [the hosted thing](https://mindcloud.co/docs/universal/rest/home/latest).

## Browse

**By letter:**
[A (185)](apis/a) · [B (146)](apis/b) · [C (285)](apis/c) · [D (170)](apis/d) · [E (131)](apis/e) · [F (136)](apis/f) · [G (117)](apis/g) · [H (89)](apis/h) · [I (94)](apis/i) · [J (25)](apis/j) · [K (47)](apis/k) · [L (123)](apis/l) · [M (167)](apis/m) · [N (86)](apis/n) · [O (94)](apis/o) · [P (251)](apis/p) · [Q (33)](apis/q) · [R (149)](apis/r) · [S (360)](apis/s) · [T (174)](apis/t) · [U (59)](apis/u) · [V (74)](apis/v) · [W (97)](apis/w) · [X (12)](apis/x) · [Y (22)](apis/y) · [Z (66)](apis/z)

**By category:**
[Communication (181)](indexes/by-category/communication.md) · [Productivity (372)](indexes/by-category/productivity.md) · [IT Operations (390)](indexes/by-category/it-operations.md) · [Sales & CRM (170)](indexes/by-category/sales-crm.md) · [Commerce (290)](indexes/by-category/commerce.md) · [Marketing (394)](indexes/by-category/marketing.md) · [Content & Files (71)](indexes/by-category/content-files.md) · [Support (180)](indexes/by-category/support.md) · [Human Resources (77)](indexes/by-category/human-resources.md) · [Business Intelligence (259)](indexes/by-category/business-intelligence.md) · [Artificial Intelligence (204)](indexes/by-category/artificial-intelligence.md) · [Website & App Building (32)](indexes/by-category/website-app-building.md) · [Other (572)](indexes/by-category/other.md)

## Missing an app? Found a bug?

[Open an issue.](https://github.com/mindcloud-inc/universal-api-reference/issues) The pipeline that maintains this library is highly automated, so new apps and fixes land fast.

## License

Documentation content is licensed [CC BY 4.0](LICENSE).

---

Built with 🤍 by [MindCloud](https://mindcloud.co).
