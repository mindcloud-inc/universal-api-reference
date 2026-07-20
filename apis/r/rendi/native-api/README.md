# Rendi: Native API Reference

A consolidated summary of Rendi's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://docs.rendi.dev/api-reference/introduction
- **API base URL:** `https://api.rendi.dev`

## Authentication

### API Key

Authenticate Rendi API requests using your API key in the X-API-KEY header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://docs.rendi.dev/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 1000; maximum 1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Command Files](actions/delete-command-files.md) | `DELETE /v1/commands/:command_id/files` | [docs](https://docs.rendi.dev/api-reference/endpoint/delete-command-files) |
| [Delete File](actions/delete-file.md) | `DELETE /v1/files/:file_id` | [docs](https://docs.rendi.dev/api-reference/endpoint/delete-file) |
| [Delete Files in Bulk](actions/delete-files-in-bulk.md) | `POST /v1/files/bulk-delete` | [docs](https://docs.rendi.dev/api-reference/endpoint/delete-files) |
| [Get File](actions/get-file.md) | `GET /v1/files/:file_id` | [docs](https://docs.rendi.dev/api-reference/endpoint/get-file) |
| [List FFmpeg Commands](actions/list-f-fmpeg-commands.md) | `GET /v1/commands` | [docs](https://docs.rendi.dev/api-reference/endpoint/list-commands) |
| [List Stored Files](actions/list-stored-files.md) | `GET /v1/files` | [docs](https://docs.rendi.dev/api-reference/endpoint/list-files) |
| [Poll FFmpeg Command](actions/poll-f-fmpeg-command.md) | `GET /v1/commands/:command_id` | [docs](https://docs.rendi.dev/api-reference/endpoint/poll-command) |
| [Run FFmpeg Command](actions/run-f-fmpeg-command.md) | `POST /v1/run-ffmpeg-command` | [docs](https://docs.rendi.dev/api-reference/endpoint/run-ffmpeg-command) |
