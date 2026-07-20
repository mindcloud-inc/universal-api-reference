# Freepik: Native API Reference

A consolidated summary of Freepik's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.freepik.com/
- **OpenAPI specification:** https://storage.googleapis.com/fc-freepik-pro-rev1-eu-api-specs/freepik-api-v1-openapi.yaml?v=13
- **API base URL:** `https://api.freepik.com`

## Authentication

### API Key

Authenticate Freepik API requests with an API key in the x-freepik-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-freepik-api-key: <apiKey>
```

[Official authentication documentation](https://docs.freepik.com/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Download Icon](actions/download-icon.md) | `GET /v1/icons/{{id}}/download` | [docs](https://docs.freepik.com/api-reference/icons/download-an-icon) |
| [Download Music](actions/download-music.md) | `GET /v1/music/{{music-id}}/download` | [docs](https://docs.freepik.com/api-reference/music/download-music) |
| [Download Resource](actions/download-resource.md) | `GET /v1/resources/{{resource-id}}/download` | [docs](https://docs.freepik.com/api-reference/resources/download-a-resource) |
| [Download Sound Effect](actions/download-sound-effect.md) | `GET /v1/sound-effects/{{sfx-id}}/download` | [docs](https://docs.freepik.com/api-reference/sound-effects/download-sound-effect) |
| [Get Icon](actions/get-icon.md) | `GET /v1/icons/{{id}}` | [docs](https://docs.freepik.com/api-reference/icons/get-one-icon-by-id) |
| [Get Music](actions/get-music.md) | `GET /v1/music/{{music-id}}` | [docs](https://docs.freepik.com/api-reference/music/get-music-by-id) |
| [Get Resource](actions/get-resource.md) | `GET /v1/resources/{{resource-id}}` | [docs](https://docs.freepik.com/api-reference/resources/images-and-templates-api) |
| [Get Resource Download Format](actions/get-resource-download-format.md) | `GET /v1/resources/{{resource-id}}/download/{{resource-format}}` | [docs](https://docs.freepik.com/api-reference/resources/images-and-templates-api) |
| [Get Sound Effect](actions/get-sound-effect.md) | `GET /v1/sound-effects/{{sfx-id}}` | [docs](https://docs.freepik.com/api-reference/sound-effects/get-sound-effect-by-id) |
| [Get Video](actions/get-video.md) | `GET /v1/videos/{{id}}` | [docs](https://docs.freepik.com/api-reference/videos/videos-api) |
| [Get Workflow App](actions/get-workflow-app.md) | `GET /v1/ai/apps/{{app-id}}` | [docs](https://docs.freepik.com/api-reference/apps/get-app) |
| [Improve Prompt](actions/improve-prompt.md) | `POST /v1/ai/improve-prompt` | [docs](https://docs.freepik.com/api-reference/improve-prompt/enhance-prompt) |
| [List LoRAs](actions/list-loras.md) | `GET /v1/ai/loras` | [docs](https://docs.freepik.com/api-reference/loras/list-loras) |
| [List My Workflow Apps](actions/list-my-workflow-apps.md) | `GET /v1/ai/me/apps` | [docs](https://docs.freepik.com/api-reference/apps/list-my-apps) |
| [List Workflow Apps](actions/list-workflow-apps.md) | `GET /v1/ai/apps` | [docs](https://docs.freepik.com/api-reference/apps/list-apps) |
| [Search Icons](actions/search-icons.md) | `GET /v1/icons` | [docs](https://docs.freepik.com/api-reference/icons/get-all-icons-by-order) |
| [Search Music](actions/search-music.md) | `GET /v1/music` | [docs](https://docs.freepik.com/api-reference/music/search-music) |
| [Search Resources](actions/search-resources.md) | `GET /v1/resources` | [docs](https://docs.freepik.com/api-reference/resources/get-all-resources) |
| [Search Sound Effects](actions/search-sound-effects.md) | `GET /v1/sound-effects` | [docs](https://docs.freepik.com/api-reference/sound-effects/search-sound-effects) |
| [Search Videos](actions/search-videos.md) | `GET /v1/videos` | [docs](https://docs.freepik.com/api-reference/videos/videos-api) |
