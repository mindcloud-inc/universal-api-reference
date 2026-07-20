# Hiflow: Native API Reference

A consolidated summary of Hiflow's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://www.hiflow.net/openapi/
- **API base URL:** `https://{account}.hiflow.net/rest`

## Authentication

### API Key

Authenticate Hiflow requests with a bearer token generated from Hiflow API keys.

### Credentials

- **API Key:** `apiKey` · required
- **Account:** `account` · required · Your Hiflow account slug from https://<account>.hiflow.net.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.hiflow.net/doc/creer-une-cle-dapi/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | `GET /customer` | [docs](https://www.hiflow.net/openapi/#tag/Customers/paths/~1customer/get) |
| [List Users](actions/list-users.md) | `GET /user` | [docs](https://www.hiflow.net/openapi/#tag/Users/paths/~1user/get) |
