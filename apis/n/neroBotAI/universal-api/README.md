# <img src="https://images.mindcloud.co/apps/icons/nero-bot-ai_1776111364905.png" alt="NeroBot AI logo" width="28" height="28"> NeroBot AI: Universal API

NeroBot AI through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/neroBotAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ai.nero.com/
- **Vendor API docs:** https://ai.nero.com/ai-api/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query AI Task Result](actions/query-ai-task-result.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/query-ai-task-result?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Get API Key Info](actions/get-api-key-info.md) | GET | Retrieves API key info from NeroBot AI. |
| [Replace API Key](actions/replace-api-key.md) | PUT | Replaces the current API key in NeroBot AI. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Avatar Styles](actions/list-avatar-styles.md) | GET | Retrieves avatar styles from NeroBot AI. |
| [List Cartoon Styles](actions/list-cartoon-styles.md) | GET | Retrieves cartoon styles from NeroBot AI. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Animate Face](actions/animate-face.md) | POST | Creates a face animation task in NeroBot AI. |
| [Change Background](actions/change-background.md) | POST | Creates a background replacement task in NeroBot AI. |
| [Colorize Photo](actions/colorize-photo.md) | POST | Creates a photo colorization task in NeroBot AI. |
| [Compress Image](actions/compress-image.md) | POST | Creates an image compression task in NeroBot AI. |
| [Count Objects](actions/count-objects.md) | POST | Creates an object counting task in NeroBot AI. |
| [Create AI Task](actions/create-ai-task.md) | POST | Creates a new AI task in NeroBot AI. |
| [Create Video from Image](actions/create-video-from-image.md) | POST | Creates an image-to-video task in NeroBot AI. |
| [Denoise Image](actions/denoise-image.md) | POST | Creates an image denoising task in NeroBot AI. |
| [Detect Faces](actions/detect-faces.md) | POST | Creates a face detection task in NeroBot AI. |
| [Fix Scratches](actions/fix-scratches.md) | POST | Creates a scratch-fixing task in NeroBot AI. |
| [Generate Avatar](actions/generate-avatar.md) | POST | Creates an avatar generation task in NeroBot AI. |
| [Generate Background](actions/generate-background.md) | POST | Creates a background generation task in NeroBot AI. |
| [Generate Background (Brick)](actions/generate-background-brick.md) | POST | Creates a brick background generation task in NeroBot AI. |
| [Generate Background (Marble)](actions/generate-background-marble.md) | POST | Creates a marble background generation task in NeroBot AI. |
| [Generate Background (Sea)](actions/generate-background-sea.md) | POST | Creates a sea background generation task in NeroBot AI. |
| [Generate Background (Wood)](actions/generate-background-wood.md) | POST | Creates a wood background generation task in NeroBot AI. |
| [Query AI Task Result](actions/query-ai-task-result.md) | GET | Retrieves an AI task result from NeroBot AI. |
| [Redraw Image](actions/redraw-image.md) | POST | Creates an image redraw task in NeroBot AI. |
| [Remove Background](actions/remove-background.md) | POST | Creates a background removal task in NeroBot AI. |
| [Restore Face](actions/restore-face.md) | POST | Creates a face restoration task in NeroBot AI. |
| [Sharpen Image](actions/sharpen-image.md) | POST | Creates an image sharpening task in NeroBot AI. |
| [Upscale Image (Anime)](actions/upscale-image-anime.md) | POST | Creates an anime image upscaling task in NeroBot AI. |
| [Upscale Image (Face Enhancement)](actions/upscale-image-face-enhancement.md) | POST | Creates a face enhancement upscaling task in NeroBot AI. |
| [Upscale Image (Iris)](actions/upscale-image-iris.md) | POST | Creates an iris detail upscaling task in NeroBot AI. |
| [Upscale Image (Photograph)](actions/upscale-image-photograph.md) | POST | Creates a photograph image upscaling task in NeroBot AI. |
| [Upscale Image (Standard)](actions/upscale-image-standard.md) | POST | Creates a standard image upscaling task in NeroBot AI. |

