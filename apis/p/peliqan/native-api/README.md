# Peliqan: Native API Reference

A consolidated summary of Peliqan's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://help.peliqan.io/peliqan-api
- **OpenAPI specification:** https://app.eu.peliqan.io/api/schema.json
- **API base URL:** `https://app.eu.peliqan.io/api`

## Authentication

### JWT API Token

Authenticate to Peliqan with a personal API token sent as Authorization: JWT {token} on every request.

[Official authentication documentation](https://help.peliqan.io/peliqan-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | `GET /user/me/` | [docs](https://app.eu.peliqan.io/api/redoc/#tag/Users/operation/user_me) |
| [List Applications](actions/list-applications.md) | `GET /applications/` | [docs](https://app.eu.peliqan.io/api/redoc/#tag/Databases/operation/list_all_applications) |
