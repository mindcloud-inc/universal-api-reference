# Creatomate: Native API Reference

A consolidated summary of Creatomate's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://creatomate.com/docs/api/reference/introduction
- **API base URL:** `https://api.creatomate.com`

## Authentication

### API Key

Use your Creatomate project API key for Bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://creatomate.com/docs/api/reference/where-can-i-find-my-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Concatenate Multiple Videos](actions/concatenate-multiple-videos.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/quick-start/concatenate-multiple-videos) |
| [Create Image From Template](actions/create-image-from-template.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/quick-start/create-a-video-by-template) |
| [Create Render](actions/create-render.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/reference/create-a-render) |
| [Create Render From RenderScript](actions/create-render-from-render-script.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/quick-start/create-a-video-by-render-script) |
| [Create Render With Metadata](actions/create-render-with-metadata.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/reference/create-a-render) |
| [Create Render With Render Scale](actions/create-render-with-render-scale.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/reference/create-a-render) |
| [Create Render With Size Constraints](actions/create-render-with-size-constraints.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/reference/create-a-render) |
| [Create Render With Template Modifications](actions/create-render-with-template-modifications.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/fundamentals/getting-started/template-modifications) |
| [Create Render With Webhook Callback](actions/create-render-with-webhook-callback.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/reference/set-up-a-webhook) |
| [Create Video From Template](actions/create-video-from-template.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/quick-start/create-a-video-by-template) |
| [Distribute Elements Over Time](actions/distribute-elements-over-time.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/quick-start/distribute-elements-over-time) |
| [Generate Image Slideshow](actions/generate-image-slideshow.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/quick-start/generate-an-image-slideshow) |
| [Generate Voiceover Video](actions/generate-voiceover-video.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/quick-start/generate-a-voice-over-video) |
| [Generate Voiceover Video With Captions](actions/generate-voiceover-video-with-captions.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/quick-start/generate-a-voice-over-video) |
| [Get Render Status](actions/get-render-status.md) | `GET /v2/renders/:render_id` | [docs](https://creatomate.com/docs/api/reference/get-the-status-of-a-render) |
| [Get Template By ID](actions/get-template-by-id.md) | `GET /v1/templates/:template_id` | [docs](https://creatomate.com/docs/api/reference/get-a-template-by-its-id) |
| [Group Elements Into Scenes](actions/group-elements-into-scenes.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/quick-start/group-elements-into-scenes) |
| [Inject RenderScript Into Template](actions/inject-render-script-into-template.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/quick-start/inject-render-script-into-a-template) |
| [List Templates](actions/list-templates.md) | `GET /v1/templates` | [docs](https://creatomate.com/docs/api/reference/get-all-templates-in-a-project) |
| [Rearrange Scenes In Template](actions/rearrange-scenes-in-template.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/quick-start/rearrange-scenes-in-a-template) |
| [Synchronize Multiple Elements](actions/synchronize-multiple-elements.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/quick-start/synchronize-multiple-elements) |
| [Use A Custom Font](actions/use-a-custom-font.md) | `POST /v2/renders` | [docs](https://creatomate.com/docs/api/quick-start/use-a-custom-font) |
