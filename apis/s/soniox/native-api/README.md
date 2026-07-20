# Soniox: Native API Reference

A consolidated summary of Soniox's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://soniox.com/docs/stt/api-reference
- **OpenAPI specification:** https://api.soniox.com/v1/openapi.json
- **API base URL:** `https://api.soniox.com/v1`

## Authentication

### API Key

Use a Soniox API key from Soniox Console.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://soniox.com/docs/stt/get-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `next_page_cursor`.

## Pagination

Use `limit` in the query string to set the page size (default 1000; accepted range 1–1000). Use `cursor` in the query string as the pagination cursor.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create transcription](actions/create-transcription.md) | `POST /transcriptions` | [docs](https://soniox.com/docs/stt/api-reference/transcriptions/create_transcription) |
| [Delete file](actions/delete-file.md) | `DELETE /files/:file_id` | [docs](https://soniox.com/docs/stt/api-reference/files/delete_file) |
| [Delete transcription](actions/delete-transcription.md) | `DELETE /transcriptions/:transcription_id` | [docs](https://soniox.com/docs/stt/api-reference/transcriptions/delete_transcription) |
| [Get file](actions/get-file.md) | `GET /files/:file_id` | [docs](https://soniox.com/docs/stt/api-reference/files/get_file) |
| [Get files](actions/get-files.md) | `GET /files` | [docs](https://soniox.com/docs/stt/api-reference/files/get_files) |
| [Get models](actions/get-models.md) | `GET /models` | [docs](https://soniox.com/docs/stt/api-reference/models/get_models) |
| [Get transcription](actions/get-transcription.md) | `GET /transcriptions/:transcription_id` | [docs](https://soniox.com/docs/stt/api-reference/transcriptions/get_transcription) |
| [Get transcription transcript](actions/get-transcription-transcript.md) | `GET /transcriptions/:transcription_id/transcript` | [docs](https://soniox.com/docs/stt/api-reference/transcriptions/get_transcription_transcript) |
| [Get transcriptions](actions/get-transcriptions.md) | `GET /transcriptions` | [docs](https://soniox.com/docs/stt/api-reference/transcriptions/get_transcriptions) |
