# Google AI Studio: Native API Reference

A consolidated summary of Google AI Studio's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://ai.google.dev/api
- **API base URL:** `https://generativelanguage.googleapis.com`

## Authentication

### Gemini API Key

Use a Gemini API key from Google AI Studio.

### Credentials

- **API Key:** `apiKey` · required · Required Gemini API key from Google AI Studio.

Send these headers with each API request:

```http
x-goog-api-key: <apiKey>
```

[Official authentication documentation](https://ai.google.dev/gemini-api/docs/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `nextPageToken`.

## Pagination

Use `pageSize` in the query string to set the page size (default 50; accepted range 1–1000). Use `pageToken` in the query string as the pagination cursor.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Batch](actions/cancel-batch.md) | `POST v1beta/batches/:name` | [docs](https://ai.google.dev/api/batch-api) |
| [Count Tokens](actions/count-tokens.md) | `POST v1beta/models/:model` | [docs](https://ai.google.dev/api/tokens) |
| [Create Cached Content](actions/create-cached-content.md) | `POST v1beta/cachedContents` | [docs](https://ai.google.dev/api/caching#method:-cachedcontents.create) |
| [Delete Batch](actions/delete-batch.md) | `DELETE v1beta/batches/:name` | [docs](https://ai.google.dev/api/batch-api) |
| [Delete Cached Content](actions/delete-cached-content.md) | `DELETE v1beta/cachedContents/:cachedContentId` | [docs](https://ai.google.dev/api/caching#method:-cachedcontents.delete) |
| [Delete File](actions/delete-file.md) | `DELETE v1beta/files/:fileId` | [docs](https://ai.google.dev/api/files#method:-files.delete) |
| [Embed Content](actions/embed-content.md) | `POST v1beta/models/:model` | [docs](https://ai.google.dev/api/embeddings) |
| [Generate Content](actions/generate-content.md) | `POST v1beta/models/:model` | [docs](https://ai.google.dev/api/generate-content) |
| [Get Batch](actions/get-batch.md) | `GET v1beta/batches/:name` | [docs](https://ai.google.dev/api/batch-api) |
| [Get Cached Content](actions/get-cached-content.md) | `GET v1beta/cachedContents/:cachedContentId` | [docs](https://ai.google.dev/api/caching#method:-cachedcontents.get) |
| [Get File](actions/get-file.md) | `GET v1beta/files/:fileId` | [docs](https://ai.google.dev/api/files#method:-files.get) |
| [Get Model](actions/get-model.md) | `GET v1beta/models/:model` | [docs](https://ai.google.dev/api/models) |
| [List Batches](actions/list-batches.md) | `GET v1beta/:name` | [docs](https://ai.google.dev/api/batch-api) |
| [List Cached Contents](actions/list-cached-contents.md) | `GET v1beta/cachedContents` | [docs](https://ai.google.dev/api/caching#method:-cachedcontents.list) |
| [List Files](actions/list-files.md) | `GET v1beta/files` | [docs](https://ai.google.dev/api/files#method:-files.list) |
| [List Models](actions/list-models.md) | `GET v1beta/models` | [docs](https://ai.google.dev/api/models) |
| [Stream Generate Content](actions/stream-generate-content.md) | `POST v1beta/models/:model` | [docs](https://ai.google.dev/api/generate-content) |
| [Update Cached Content](actions/update-cached-content.md) | `PATCH v1beta/cachedContents/:cachedContentId` | [docs](https://ai.google.dev/api/caching#method:-cachedcontents.patch) |
