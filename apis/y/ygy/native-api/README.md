# y.gy: Native API Reference

A consolidated summary of y.gy's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://app.y.gy/docs
- **API base URL:** `https://api.y.gy`

## Authentication

### API Key

Use a y.gy API key from the account dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.y.gy/docs/api-docs/authenticate)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 25). Use `offset` in the query string as the record offset.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Short Link](actions/create-short-link.md) | `POST /api/v1/link` | [docs](https://app.y.gy/docs/api-docs/links) |
| [Create Tag](actions/create-tag.md) | `POST /api/v1/tag` | [docs](https://app.y.gy/docs/api-docs/tags) |
| [Delete Short Link](actions/delete-short-link.md) | `DELETE /api/v1/link/:id` | [docs](https://app.y.gy/docs/api-docs/links) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /api/v1/tag/:id` | [docs](https://app.y.gy/docs/api-docs/tags) |
| [Get Short Link](actions/get-short-link.md) | `GET /api/v1/link/:id` | [docs](https://app.y.gy/docs/api-docs/links) |
| [List Links](actions/list-links.md) | `GET /api/v1/link` | [docs](https://app.y.gy/docs/api-docs/links) |
| [List Tags](actions/list-tags.md) | `GET /api/v1/tag` | [docs](https://app.y.gy/docs/api-docs/tags) |
| [Update Short Link](actions/update-short-link.md) | `PATCH /api/v1/link/:id` | [docs](https://app.y.gy/docs/api-docs/links) |
