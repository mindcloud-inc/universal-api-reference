# Mem: Native API Reference

A consolidated summary of Mem's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.mem.ai/api-reference/overview/introduction
- **API base URL:** `https://api.mem.ai`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.mem.ai/api-reference/overview/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50).

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | `POST /v2/collections` | [docs](https://docs.mem.ai/api-reference/collections/create-collection) |
| [Create Note](actions/create-note.md) | `POST /v2/notes` | [docs](https://docs.mem.ai/api-reference/notes/create-note) |
| [Delete Collection](actions/delete-collection.md) | `DELETE /v2/collections/:collectionId` | [docs](https://docs.mem.ai/api-reference/collections/delete-collection) |
| [Delete Note](actions/delete-note.md) | `DELETE /v2/notes/:noteId` | [docs](https://docs.mem.ai/api-reference/notes/delete-note) |
| [Get Collection](actions/get-collection.md) | `GET /v2/collections/:collectionId` | [docs](https://docs.mem.ai/api-reference/collections/read-collection) |
| [Get Note](actions/get-note.md) | `GET /v2/notes/:noteId` | [docs](https://docs.mem.ai/api-reference/notes/read-note) |
| [List Collections](actions/list-collections.md) | `GET /v2/collections` | [docs](https://docs.mem.ai/api-reference/collections/list-collections) |
| [List Notes](actions/list-notes.md) | `GET /v2/notes` | [docs](https://docs.mem.ai/api-reference/notes/list-notes) |
| [Mem It](actions/mem-it.md) | `POST /v2/mem-it` | [docs](https://docs.mem.ai/api-reference/mem-it/mem-it) |
| [Search Collections](actions/search-collections.md) | `POST /v2/collections/search` | [docs](https://docs.mem.ai/api-reference/collections/search-collections) |
| [Search Notes](actions/search-notes.md) | `POST /v2/notes/search` | [docs](https://docs.mem.ai/api-reference/notes/search-notes) |
