# Beatoven AI: Native API Reference

A consolidated summary of Beatoven AI's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://github.com/Beatoven/public-api/blob/main/docs/api-spec.md
- **API base URL:** `https://public-api.beatoven.ai/api/v1`

## Authentication

### API Key

Use your Beatoven AI API key. The platform injects it as Authorization: Bearer <apiKey>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://github.com/Beatoven/public-api/blob/main/docs/api-spec.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Compose Track](actions/compose-track.md) | `POST /tracks/compose` | [docs](https://github.com/Beatoven/public-api/blob/main/docs/api-spec.md) |
| [Create Track](actions/create-track.md) | `POST /tracks` | [docs](https://raw.githubusercontent.com/Beatoven/public-api/main/docs/api-spec-old.md) |
| [Get Task Status](actions/get-task-status.md) | `GET /tasks/:taskId` | [docs](https://github.com/Beatoven/public-api/blob/main/docs/api-spec.md) |
