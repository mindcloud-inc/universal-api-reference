# Rye: Native API Reference

A consolidated summary of Rye's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://rye.com/docs/api-v2/introduction
- **API base URL:** `https://staging.api.rye.com`

## Authentication

### API Key

Authenticate to Rye's Universal Checkout REST API with the staging API key sent as an Authorization bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://rye.com/docs/api-v2/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The next-page cursor is read from `pageInfo.endCursor`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `after` in the query string as the pagination cursor.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Payment To Checkout Intent](actions/add-payment-to-checkout-intent.md) | `POST /api/v1/checkout-intents/{id}/payment` | [docs](https://rye.com/docs/api-v2/introduction) |
| [Confirm Checkout Intent](actions/confirm-checkout-intent.md) | `POST /api/v1/checkout-intents/{id}/confirm` | [docs](https://rye.com/docs/api-v2/introduction) |
| [Create Checkout Intent](actions/create-checkout-intent.md) | `POST /api/v1/checkout-intents` | [docs](https://rye.com/docs/api-v2/introduction) |
| [Create Checkout Session](actions/create-checkout-session.md) | `POST /api/v1/betas/checkout-sessions` | [docs](https://rye.com/docs/api-v2/introduction) |
| [Create Payment Gateway Session](actions/create-payment-gateway-session.md) | `POST /api/v1/payment-gateways/{gateway}/session` | [docs](https://rye.com/docs/api-v2/introduction) |
| [Create Top-Up Invoice](actions/create-top-up-invoice.md) | `POST /api/v1/billing/drawdown/topup` | [docs](https://rye.com/docs/api-v2/introduction) |
| [Get Balance](actions/get-balance.md) | `GET /api/v1/billing/balance` | [docs](https://rye.com/docs/api-v2/introduction) |
| [Get Billing Info](actions/get-billing-info.md) | `GET /api/v1/billing` | [docs](https://rye.com/docs/api-v2/introduction) |
| [Get Brand By Domain](actions/get-brand-by-domain.md) | `GET /api/v1/brands/domain/{domain}` | [docs](https://rye.com/docs/api-v2/introduction) |
| [Get Checkout Intent](actions/get-checkout-intent.md) | `GET /api/v1/checkout-intents/{id}` | [docs](https://rye.com/docs/api-v2/introduction) |
| [Get Shipment](actions/get-shipment.md) | `GET /api/v1/shipments/{id}` | [docs](https://rye.com/docs/api-v2/introduction) |
| [List Checkout Intent Shipments](actions/list-checkout-intent-shipments.md) | `GET /api/v1/checkout-intents/{id}/shipments` | [docs](https://rye.com/docs/api-v2/introduction) |
| [List Checkout Intents](actions/list-checkout-intents.md) | `GET /api/v1/checkout-intents` | [docs](https://rye.com/docs/api-v2/introduction) |
| [List Shipments](actions/list-shipments.md) | `GET /api/v1/shipments` | [docs](https://rye.com/docs/api-v2/introduction) |
| [List Transactions](actions/list-transactions.md) | `GET /api/v1/billing/transactions` | [docs](https://rye.com/docs/api-v2/introduction) |
| [Lookup Product](actions/lookup-product.md) | `GET /api/v1/products/lookup` | [docs](https://rye.com/docs/api-v2/introduction) |
| [Purchase Product](actions/purchase-product.md) | `POST /api/v1/checkout-intents/purchase` | [docs](https://rye.com/docs/api-v2/introduction) |
| [Setup Drawdown Billing](actions/setup-drawdown-billing.md) | `POST /api/v1/billing/drawdown` | [docs](https://rye.com/docs/api-v2/introduction) |
