# Chargeblast: Native API Reference

A consolidated summary of Chargeblast's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://docs.chargeblast.com/api-reference/getting-started/guide
- **OpenAPI specification:** https://docs.chargeblast.com/openapi.json
- **API base URL:** `https://api.chargeblast.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.chargeblast.com/api-reference/introduction/authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Fetch Alerts](actions/fetch-alerts.md) | `GET /api/v2/alerts` | [docs](https://docs.chargeblast.com/api-reference/alerts/fetch-alerts) |
| [Fetch Deflection Logs](actions/fetch-deflection-logs.md) | `GET /api/v3/deflections/logs` | [docs](https://docs.chargeblast.com/api-reference/deflections/logs) |
| [Fetch Descriptors](actions/fetch-descriptors.md) | `GET /api/descriptors` | [docs](https://docs.chargeblast.com/api-reference/enrollment/fetch-descriptors) |
| [Fetch Merchant](actions/fetch-merchant.md) | `GET /api/merchant` | [docs](https://docs.chargeblast.com/api-reference/enrollment/fetch-merchant) |
| [Fetch Merchants](actions/fetch-merchants.md) | `GET /api/v2/merchants` | [docs](https://docs.chargeblast.com/api-reference/enrollment/fetch-merchants) |
| [Fetch Order](actions/fetch-order.md) | `GET /api/v2/orders/:id` | [docs](https://docs.chargeblast.com/api-reference/sync-data/get-order) |
| [Fetch Orders](actions/fetch-orders.md) | `GET /api/v2/orders` | [docs](https://docs.chargeblast.com/api-reference/sync-data/get-orders) |
| [Upload IP Data](actions/upload-ip-data.md) | `POST /api/v2/track` | [docs](https://docs.chargeblast.com/api-reference/sync-data/track) |
| [Upload Orders](actions/upload-orders.md) | `POST /api/v2/orders/upload` | [docs](https://docs.chargeblast.com/api-reference/sync-data/upload-orders) |
