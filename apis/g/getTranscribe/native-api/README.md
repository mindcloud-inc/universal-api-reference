# GetTranscribe: Native API Reference

A consolidated summary of GetTranscribe's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://www.gettranscribe.ai/api-documentation/authentication
- **API base URL:** `https://api.gettranscribe.ai`

## Authentication

### API Key

Custom API key auth for providers that require a non-bearer request shape.

### Credentials

- **API Key:** `apiKey` · optional · Your GetTranscribe tenant API key.

[Official authentication documentation](https://www.gettranscribe.ai/api-documentation/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `$limit` in the query string to set the page size (default 50; accepted range 1–100). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | `POST /transcriptions-folders` | [docs](https://www.gettranscribe.ai/api-documentation/folders/create) |
| [Create Transcription](actions/create-transcription.md) | `POST /transcriptions` | [docs](https://www.gettranscribe.ai/api-documentation/transcriptions/create) |
| [Get Transcription](actions/get-transcription.md) | `GET /transcriptions/:id` | [docs](https://www.gettranscribe.ai/api-documentation/transcriptions/get) |
| [Get User Info](actions/get-user-info.md) | `GET /users/:id` | [docs](https://www.gettranscribe.ai/api-documentation/user/get) |
| [List Folders](actions/list-folders.md) | `GET /transcriptions-folders` | [docs](https://www.gettranscribe.ai/api-documentation/folders/list) |
| [List Transcriptions](actions/list-transcriptions.md) | `GET /transcriptions` | [docs](https://www.gettranscribe.ai/api-documentation/transcriptions/list) |
| [Update Folder](actions/update-folder.md) | `PATCH /transcriptions-folders/:id` | [docs](https://www.gettranscribe.ai/api-documentation/folders/update) |
