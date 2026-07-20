# Fliz: Native API Reference

A consolidated summary of Fliz's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://app.fliz.ai/api-docs
- **OpenAPI specification:** https://app.fliz.ai/api/openapi
- **API base URL:** `https://app.fliz.ai`

## Authentication

### API Token

Use a Fliz API token as a Bearer token.

### Credentials

- **API token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.fliz.ai/api-docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create video](actions/create-video.md) | `POST /api/rest/video` | [docs](https://app.fliz.ai/api-docs) |
| [Get video](actions/get-video.md) | `GET /api/rest/videos/:id` | [docs](https://app.fliz.ai/api-docs) |
| [List musics](actions/list-musics.md) | `GET /api/rest/musics` | [docs](https://app.fliz.ai/api-docs) |
| [List videos](actions/list-videos.md) | `GET /api/rest/videos` | [docs](https://app.fliz.ai/api-docs) |
| [List voices](actions/list-voices.md) | `GET /api/rest/voices` | [docs](https://app.fliz.ai/api-docs) |
| [Translate video](actions/translate-video.md) | `POST /api/rest/videos/:from_video_id/translate` | [docs](https://app.fliz.ai/api-docs) |
