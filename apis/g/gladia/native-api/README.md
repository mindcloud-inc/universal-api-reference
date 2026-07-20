# Gladia: Native API Reference

A consolidated summary of Gladia's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.gladia.io/api-reference
- **OpenAPI specification:** https://api.gladia.io/openapi.json
- **API base URL:** `https://api.gladia.io`

## Authentication

### API Key

Use your Gladia API key from app.gladia.io.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-gladia-key: <apiKey>
```

[Official authentication documentation](https://docs.gladia.io/api-reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `next`.

## Pagination

Use `limit` in the query string to set the page size (default 20; minimum 1). Use `offset` in the query string as the record offset.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Legacy Audio Transcription](actions/create-legacy-audio-transcription.md) | `POST /audio/text/audio-transcription` | [docs](https://docs.gladia.io/chapters/pre-recorded-stt/migration-from-v1) |
| [Create Legacy Video Transcription](actions/create-legacy-video-transcription.md) | `POST /video/text/video-transcription` | [docs](https://api.gladia.io/openapi.json) |
| [Create Live Job](actions/create-live-job.md) | `POST /v2/live` | [docs](https://docs.gladia.io/api-reference/v2/live/init) |
| [Create Pre-recorded Transcription](actions/create-pre-recorded-transcription.md) | `POST /v2/pre-recorded` | [docs](https://docs.gladia.io/api-reference/v2/pre-recorded/init) |
| [Create Transcription](actions/create-transcription.md) | `POST /v2/transcription` | [docs](https://docs.gladia.io/api-reference/v2/transcription/init) |
| [Delete Live Job](actions/delete-live-job.md) | `DELETE /v2/live/:id` | [docs](https://docs.gladia.io/api-reference/v2/live/delete) |
| [Delete Pre-recorded Transcription](actions/delete-pre-recorded-transcription.md) | `DELETE /v2/pre-recorded/:id` | [docs](https://docs.gladia.io/api-reference/v2/pre-recorded/delete) |
| [Delete Transcription](actions/delete-transcription.md) | `DELETE /v2/transcription/:id` | [docs](https://docs.gladia.io/api-reference/v2/transcription/delete) |
| [Download Live Audio File](actions/download-live-audio-file.md) | `GET /v2/live/:id/file` | [docs](https://docs.gladia.io/api-reference/v2/live/get-audio) |
| [Download Pre-recorded Audio File](actions/download-pre-recorded-audio-file.md) | `GET /v2/pre-recorded/:id/file` | [docs](https://docs.gladia.io/api-reference/v2/pre-recorded/get-audio) |
| [Download Transcription Audio File](actions/download-transcription-audio-file.md) | `GET /v2/transcription/:id/file` | [docs](https://docs.gladia.io/api-reference/v2/transcription/get-audio) |
| [Get Live Job](actions/get-live-job.md) | `GET /v2/live/:id` | [docs](https://docs.gladia.io/api-reference/v2/live/get) |
| [Get Pre-recorded Transcription](actions/get-pre-recorded-transcription.md) | `GET /v2/pre-recorded/:id` | [docs](https://docs.gladia.io/api-reference/v2/pre-recorded/get) |
| [Get Transcription](actions/get-transcription.md) | `GET /v2/transcription/:id` | [docs](https://docs.gladia.io/api-reference/v2/transcription/get) |
| [List Job History](actions/list-job-history.md) | `GET /v1/history` | [docs](https://api.gladia.io/openapi.json) |
| [List Live Jobs](actions/list-live-jobs.md) | `GET /v2/live` | [docs](https://docs.gladia.io/api-reference/v2/live/list) |
| [List Pre-recorded Transcriptions](actions/list-pre-recorded-transcriptions.md) | `GET /v2/pre-recorded` | [docs](https://docs.gladia.io/api-reference/v2/pre-recorded/list) |
| [List Transcriptions](actions/list-transcriptions.md) | `GET /v2/transcription` | [docs](https://docs.gladia.io/api-reference/v2/transcription/list) |
| [Update Live Job Debug Params](actions/update-live-job-debug-params.md) | `PATCH /v2/live/:id` | [docs](https://api.gladia.io/openapi.json) |
| [Upload Audio File](actions/upload-audio-file.md) | `POST /v2/upload` | [docs](https://docs.gladia.io/api-reference/v2/upload/audio-file) |
