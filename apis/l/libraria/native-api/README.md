# Libraria: Native API Reference

A consolidated summary of Libraria's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://docs.libraria.ai/api-reference/home
- **API base URL:** `https://api.libraria.ai`

## Authentication

### API Key

Use a Libraria API key in the Authorization Bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.libraria.ai/api-reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Document](actions/add-document.md) | `POST /library/:library_id/document` | [docs](https://docs.libraria.ai/api-reference/library/create-document) |
| [Create Query](actions/create-query.md) | `POST /v2/library/:library_id/query` | [docs](https://docs.libraria.ai/api-reference/library-v2/create-query) |
| [Create Query (Legacy)](actions/create-query-legacy.md) | `POST /library/:library_id/query` | [docs](https://docs.libraria.ai/api-reference/library/create-query) |
| [Delete Document](actions/delete-document.md) | `DELETE /library/:library_id/document/:document_id` | [docs](https://docs.libraria.ai/api-reference/library/delete-document) |
| [Get Document](actions/get-document.md) | `GET /library/:library_id/document/:document_id` | [docs](https://docs.libraria.ai/api-reference/library/get-document) |
