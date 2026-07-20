# Split CSV: Native API Reference

A consolidated summary of Split CSV's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://www.splitcsv.com/developers/core/
- **API base URL:** `https://www.splitcsv.com`

## Authentication

### Personal API Token

Connect using a Split CSV personal API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.splitcsv.com/developers/core/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | `POST /app/api/v1/orders` | [docs](https://www.splitcsv.com/developers/core/) |
| [Get Order Status](actions/get-order-status.md) | `GET /app/api/v1/orders/:id/status` | [docs](https://www.splitcsv.com/developers/core/) |
| [Retrieve Profile](actions/retrieve-profile.md) | `GET /app/v1/account/profile` | [docs](https://www.splitcsv.com/developers/core/) |
