# Strale: Native API Reference

A consolidated summary of Strale's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://strale.dev/docs
- **OpenAPI specification:** https://api.strale.io/openapi.json
- **API base URL:** `https://api.strale.io`

## Authentication

### API Key

Connect Strale with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://strale.dev/docs#auth)

## API conventions

Responses from this API use JSON.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Wallet Top-Up](actions/create-wallet-top-up.md) | `POST /v1/wallet/topup` | [docs](https://api.strale.io/openapi.json) |
| [Execute Capability](actions/execute-capability.md) | `POST /v1/do` | [docs](https://strale.dev/docs#api-do) |
| [Execute Task](actions/execute-task.md) | `POST /v1/do` | [docs](https://strale.dev/docs#api-do) |
| [Get Capability](actions/get-capability.md) | `GET /v1/capabilities/:slug` | [docs](https://strale.dev/docs#api-capabilities) |
| [Get Capability Quality](actions/get-capability-quality.md) | `GET /v1/quality/:slug` | [docs](https://strale.dev/docs#api-quality) |
| [Get Solution](actions/get-solution.md) | `GET /v1/solutions/:slug` | [docs](https://strale.dev/docs#api-solutions) |
| [Get Transaction](actions/get-transaction.md) | `GET /v1/transactions/:id` | [docs](https://api.strale.io/openapi.json) |
| [Get Wallet Balance](actions/get-wallet-balance.md) | `GET /v1/wallet/balance` | [docs](https://strale.dev/docs#api-balance) |
| [List Capabilities](actions/list-capabilities.md) | `GET /v1/capabilities` | [docs](https://strale.dev/docs#api-capabilities) |
| [List Solutions](actions/list-solutions.md) | `GET /v1/solutions` | [docs](https://strale.dev/docs#api-solutions) |
| [List Transactions](actions/list-transactions.md) | `GET /v1/transactions` | [docs](https://api.strale.io/openapi.json) |
| [List Wallet Transactions](actions/list-wallet-transactions.md) | `GET /v1/wallet/transactions` | [docs](https://api.strale.io/openapi.json) |
| [Reissue Audit Token](actions/reissue-audit-token.md) | `POST /v1/transactions/:id/audit-token` | [docs](https://api.strale.io/openapi.json) |
| [Suggest Capability](actions/suggest-capability.md) | `POST /v1/suggest` | [docs](https://strale.dev/docs#api-suggest) |
| [Typeahead Search](actions/typeahead-search.md) | `GET /v1/suggest/typeahead` | [docs](https://strale.dev/docs#api-suggest) |
| [Verify Transaction Integrity](actions/verify-transaction-integrity.md) | `GET /v1/verify/:transactionId` | [docs](https://api.strale.io/openapi.json) |
