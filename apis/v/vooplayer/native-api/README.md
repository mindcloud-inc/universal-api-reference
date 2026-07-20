# Vooplayer: Native API Reference

A consolidated summary of Vooplayer's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://app.spotlightr.com/docs/api/
- **API base URL:** `https://api.spotlightr.com`

## Authentication

### API Key

Connect with your Spotlightr API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.spotlightr.com/docs/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Whitelisted Domain](actions/add-whitelisted-domain.md) | `POST /api/user/domain` | [docs](https://app.spotlightr.com/docs/api/#addDomain) |
| [Create Project](actions/create-project.md) | `POST /groups` | [docs](https://app.spotlightr.com/docs/api/#groups) |
| [Create Video](actions/create-video.md) | `POST /api/createVideo` | [docs](https://app.spotlightr.com/docs/api/#create-video) |
| [Delete Videos](actions/delete-videos.md) | `POST /api/deleteVideo` | [docs](https://app.spotlightr.com/docs/api/#deleteVideo) |
| [Get Video Metrics](actions/get-video-metrics.md) | `GET /api/video/metrics` | [docs](https://app.spotlightr.com/docs/api/#metrics) |
| [Get Video Views](actions/get-video-views.md) | `GET /api/views/getViews` | [docs](https://app.spotlightr.com/docs/api/#getViews) |
| [Global Search](actions/global-search.md) | `POST /search/global` | [docs](https://app.spotlightr.com/docs/api/#search) |
| [List Projects](actions/list-projects.md) | `GET /groups` | [docs](https://app.spotlightr.com/docs/api/#groups) |
| [List Videos](actions/list-videos.md) | `GET /api/videos` | [docs](https://app.spotlightr.com/docs/api/#videos) |
| [List Whitelisted Domains](actions/list-whitelisted-domains.md) | `GET /api/user/domain` | [docs](https://app.spotlightr.com/docs/api/#getDomain) |
| [Set Video Source](actions/set-video-source.md) | `GET /api/videoSource` | [docs](https://app.spotlightr.com/docs/api/#videoSource) |
| [Update Video Player Settings](actions/update-video-player-settings.md) | `POST /video/updateSettings` | [docs](https://app.spotlightr.com/docs/api/#updatePlayerSettings) |
