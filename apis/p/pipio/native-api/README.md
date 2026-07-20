# Pipio: Native API Reference

A consolidated summary of Pipio's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.pipio.ai
- **API base URL:** `https://avatar.pipio.ai`

## Authentication

### API Key

Authenticate Pipio requests with an API key from your Pipio account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.pipio.ai/reference/getting-started-with-your-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `pageSize` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Dubbed Video Legacy](actions/generate-dubbed-video-legacy.md) | `POST https://project.pipio.ai/project/generate/dubbing` | [docs](https://docs.pipio.ai/generate-dubbed-video-tutorial) |
| [Generate Dubbed Video V2](actions/generate-dubbed-video-v2.md) | `POST https://project.pipio.ai/project/generate/dubbing/v2` | [docs](https://docs.pipio.ai/dubbing-v2) |
| [Generate Lip Sync Video](actions/generate-lip-sync-video.md) | `POST https://project.pipio.ai/project/generate/lipsync` | [docs](https://docs.pipio.ai/lip-sync-v1) |
| [Generate Single Clip Video](actions/generate-single-clip-video.md) | `POST https://generate.pipio.ai/single-clip` | [docs](https://docs.pipio.ai/generate-video) |
| [List Avatars](actions/list-avatars.md) | `GET /actor` | [docs](https://docs.pipio.ai/avatar-list) |
| [List Ethnicities](actions/list-ethnicities.md) | `GET /actor/ethnicities/all` | [docs](https://docs.pipio.ai/ethnicity-list) |
| [List Languages](actions/list-languages.md) | `GET /actor/languages/all` | [docs](https://docs.pipio.ai/language-list) |
| [List Videos](actions/list-videos.md) | `GET https://generate.pipio.ai/single-clip` | [docs](https://docs.pipio.ai/list-videos) |
| [List Voices](actions/list-voices.md) | `GET /voice` | [docs](https://docs.pipio.ai/voice-list) |
| [Retrieve Video](actions/retrieve-video.md) | `GET https://generate.pipio.ai/single-clip/:id` | [docs](https://docs.pipio.ai/get-video) |
