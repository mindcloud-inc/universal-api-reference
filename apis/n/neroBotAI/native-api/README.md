# NeroBot AI: Native API Reference

A consolidated summary of NeroBot AI's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://ai.nero.com/ai-api/docs/
- **API base URL:** `https://api.nero.com`

## Authentication

### API Key

Provider auth uses the `x-neroai-api-key` header. The primary credential remains platform-managed as `credentials.apiKey` and request headers must map it to the Nero header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-neroai-api-key: <apiKey>
```

[Official authentication documentation](https://ai.nero.com/ai-api/docs/#authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Animate Face](actions/animate-face.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Change Background](actions/change-background.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Colorize Photo](actions/colorize-photo.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Compress Image](actions/compress-image.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Count Objects](actions/count-objects.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Create AI Task](actions/create-ai-task.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Create Video from Image](actions/create-video-from-image.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Denoise Image](actions/denoise-image.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Detect Faces](actions/detect-faces.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Fix Scratches](actions/fix-scratches.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Generate Avatar](actions/generate-avatar.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Generate Background](actions/generate-background.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Generate Background (Brick)](actions/generate-background-brick.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Generate Background (Marble)](actions/generate-background-marble.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Generate Background (Sea)](actions/generate-background-sea.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Generate Background (Wood)](actions/generate-background-wood.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Get API Key Info](actions/get-api-key-info.md) | `GET /biz/api/apikey` | [docs](https://ai.nero.com/ai-api/docs/) |
| [List Avatar Styles](actions/list-avatar-styles.md) | `GET /biz/api/avatar/styles` | [docs](https://ai.nero.com/ai-api/docs/) |
| [List Cartoon Styles](actions/list-cartoon-styles.md) | `GET /biz/api/cartoon/styles` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Query AI Task Result](actions/query-ai-task-result.md) | `GET /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Redraw Image](actions/redraw-image.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Remove Background](actions/remove-background.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Replace API Key](actions/replace-api-key.md) | `PUT /biz/api/apikey/replace` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Restore Face](actions/restore-face.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Sharpen Image](actions/sharpen-image.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Upscale Image (Anime)](actions/upscale-image-anime.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Upscale Image (Face Enhancement)](actions/upscale-image-face-enhancement.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Upscale Image (Iris)](actions/upscale-image-iris.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Upscale Image (Photograph)](actions/upscale-image-photograph.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
| [Upscale Image (Standard)](actions/upscale-image-standard.md) | `POST /biz/api/task` | [docs](https://ai.nero.com/ai-api/docs/) |
