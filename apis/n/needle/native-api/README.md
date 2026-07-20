# Needle: Native API Reference

A consolidated summary of Needle's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.needle.app/docs/api-reference/needle-api/
- **API base URL:** `https://needle.app`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.needle.app/docs/api-reference/needle-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `result`.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Files To Collection](actions/add-files-to-collection.md) | `POST /api/v1/collections/:collectionId/files` | [docs](https://docs.needle.app/docs/api-reference/add-files-to-collection/) |
| [Create Collection](actions/create-collection.md) | `POST /api/v1/collections` | [docs](https://docs.needle.app/docs/api-reference/create-collection/) |
| [Delete Files From Collection](actions/delete-files-from-collection.md) | `DELETE /api/v1/collections/:collectionId/files` | [docs](https://docs.needle.app/docs/api-reference/delete-files-from-collection/) |
| [Get Collection Details](actions/get-collection-details.md) | `GET /api/v1/collections/:collectionId` | [docs](https://docs.needle.app/docs/api-reference/get-collection/) |
| [Get Collection Stats](actions/get-collection-stats.md) | `GET /api/v1/collections/:collectionId/stats` | [docs](https://docs.needle.app/docs/api-reference/get-collection-stats/) |
| [Get File Download URL](actions/get-file-download-url.md) | `GET /api/v1/files/:fileId/download_url` | [docs](https://docs.needle.app/docs/api-reference/get-download-url/) |
| [Get File Upload URL](actions/get-file-upload-url.md) | `GET /api/v1/files/upload_url` | [docs](https://docs.needle.app/docs/api-reference/get-upload-url/) |
| [List Collection Files](actions/list-collection-files.md) | `GET /api/v1/collections/:collectionId/files` | [docs](https://docs.needle.app/docs/api-reference/list-collection-files/) |
| [List Collections](actions/list-collections.md) | `GET /api/v1/collections` | [docs](https://docs.needle.app/docs/api-reference/list-collections/) |
| [Search Collection](actions/search-collection.md) | `POST https://search.needle.app/api/v1/collections/:collectionId/search` | [docs](https://docs.needle.app/docs/api-reference/search-collection/) |
