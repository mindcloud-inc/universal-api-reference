# Opinion Stage: Native API Reference

A consolidated summary of Opinion Stage's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://api.opinionstage.com/api-docs/index.html
- **OpenAPI specification:** https://api.opinionstage.com/api-docs/api/v2/openapi.yaml
- **API base URL:** `https://api.opinionstage.com`

## Authentication

### API Key

Use your Opinion Stage API key. Runtime will send it as HTTP Basic auth with a blank password.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.opinionstage.com/api-docs/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The current page number is read from `meta.page.current`.

## Pagination

Use `page[size]` in the query string to set the page size. Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Items](actions/list-items.md) | `GET /api/v2/items` | [docs](https://api.opinionstage.com/api-docs/index.html) |
