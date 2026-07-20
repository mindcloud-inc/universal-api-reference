# IFTTT: Native API Reference

A consolidated summary of IFTTT's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://ifttt.com/docs/connect_api
- **API base URL:** `https://connect.ifttt.com`

## Authentication

### IFTTT Service Key

Authenticate with an IFTTT Connect API service key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
IFTTT-Service-Key: <apiKey>
```

[Official authentication documentation](https://ifttt.com/docs/connect_api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the request body to set the page size. Use `cursor` in the request body as the pagination cursor.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current Service and User](actions/get-current-service-and-user.md) | `GET /v2/me` | [docs](https://ifttt.com/docs/connect_api) |
