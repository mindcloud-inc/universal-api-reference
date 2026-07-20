# 1Shot: Native API Reference

A consolidated summary of 1Shot's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.1shotapi.com/api/index.html
- **OpenAPI specification:** https://docs.1shotapi.com/_static/m2mGatewaySpec.yaml
- **API base URL:** `https://api.1shotapi.com/v0`

## Authentication

### OAuth 2.0

Connect to 1Shot API using OAuth 2.0 client credentials (machine-to-machine).

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.1shotapi.com/v0/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read:api write:api`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.1shotapi.com/api/api.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `page`.

## Pagination

Use `pageSize` in the query string to set the page size (default 25). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contract Event](actions/create-contract-event.md) | `POST /business/:businessId/events` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Create Contract Method](actions/create-contract-method.md) | `POST /business/:businessId/methods` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Create Delegation](actions/create-delegation.md) | `POST /wallets/:walletId/delegations` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Create Wallet](actions/create-wallet.md) | `POST /business/:businessId/wallets` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Encode Contract Method](actions/encode-contract-method.md) | `POST /methods/:contractMethodId/encode` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Estimate Contract Method](actions/estimate-contract-method.md) | `POST /methods/:contractMethodId/estimate` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Execute Contract Method](actions/execute-contract-method.md) | `POST /methods/:contractMethodId/execute` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Get Chain Fees](actions/get-chain-fees.md) | `GET /chains/:chainId/fees` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Get Contract Event](actions/get-contract-event.md) | `GET /events/:contractEventId` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Get Contract Method](actions/get-contract-method.md) | `GET /methods/:contractMethodId` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Get Transaction](actions/get-transaction.md) | `GET /transactions/:transactionId` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Get Wallet](actions/get-wallet.md) | `GET /wallets/:walletId` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Inspect Contract](actions/inspect-contract.md) | `GET /chains/:chainId/contracts/:contractAddress` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [List Chains](actions/list-chains.md) | `GET /chains` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [List Contract Events](actions/list-contract-events.md) | `GET /business/:businessId/events` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [List Contract Methods](actions/list-contract-methods.md) | `GET /business/:businessId/methods` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [List Delegations](actions/list-delegations.md) | `GET /wallets/:walletId/delegations` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [List Transactions](actions/list-transactions.md) | `GET /business/:businessId/transactions` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [List Wallets](actions/list-wallets.md) | `GET /business/:businessId/wallets` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | `GET /business/:businessId/webhooks/endpoints` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [List Webhook Triggers](actions/list-webhook-triggers.md) | `GET /business/:businessId/webhooks/triggers` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Search Contract Event Logs](actions/search-contract-event-logs.md) | `POST /events/:contractEventId/search` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Test Contract Method](actions/test-contract-method.md) | `POST /methods/:contractMethodId/test` | [docs](https://docs.1shotapi.com/api/openapi.html) |
| [Transfer Native Token](actions/transfer-native-token.md) | `POST /wallets/:walletId/transfer` | [docs](https://docs.1shotapi.com/api/openapi.html) |
