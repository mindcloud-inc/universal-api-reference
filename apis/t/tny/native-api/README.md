# Tny: Native API Reference

A consolidated summary of Tny's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://www.tny.dev/api-docs
- **OpenAPI specification:** https://www.tny.dev/api/v1/openapi
- **API base URL:** `https://www.tny.dev`

## Authentication

### API Key

Authenticate Tny requests with an API key sent in the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://www.tny.dev/api-docs#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `links`. The total page count is read from `pagination.totalPages`. The current page number is read from `pagination.page`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Create Short Links](actions/bulk-create-short-links.md) | `POST /api/v1/shorten/bulk` | [docs](https://www.tny.dev/api-docs#bulk-shorten) |
| [Create Short Link](actions/create-short-link.md) | `POST /api/v1/shorten` | [docs](https://www.tny.dev/api-docs#create-short-link) |
| [Get Link Analytics](actions/get-link-analytics.md) | `GET /api/v1/analytics/:slug` | [docs](https://www.tny.dev/api-docs#get-analytics) |
| [List Links](actions/list-links.md) | `GET /api/v1/links` | [docs](https://www.tny.dev/api-docs#list-links) |
