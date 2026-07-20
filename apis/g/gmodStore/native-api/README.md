# GmodStore: Native API Reference

A consolidated summary of GmodStore's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.pivity.com
- **OpenAPI specification:** https://www.gmodstore.com/openapi
- **API base URL:** `https://api.pivity.com/v3`

## Authentication

### Personal Access Token

Use a GmodStore personal access token. MindCloud sends it as a bearer token and scopes requests to GmodStore with the tenant header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.pivity.com)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `perPage` in the query string to set the page size (default 24; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Filtering

Send filters in the query string.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://docs.pivity.com) |
