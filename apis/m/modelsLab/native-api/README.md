# ModelsLab: Native API Reference

A consolidated summary of ModelsLab's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.modelslab.com
- **API base URL:** `https://modelslab.com/api`

## Authentication

### API Key

Authenticate ModelsLab standard API requests with an API key supplied as the `key` field in the JSON request body.

### Credentials

- **API key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.modelslab.com/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,503`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Caption Image](actions/caption-image.md) | `POST /v6/image_editing/caption` | [docs](https://docs.modelslab.com/image-editing/caption) |
| [Check Processing Requests](actions/check-processing-requests.md) | `POST /v6/processing/request_count` | [docs](https://docs.modelslab.com/general-api/check-requests) |
| [Check Prompt Safety](actions/check-prompt-safety.md) | `POST /check_nsfw_cp` | [docs](https://docs.modelslab.com/general-api/nsfw-prompt-check) |
| [Design Interior](actions/design-interior.md) | `POST /v6/interior/make` | [docs](https://docs.modelslab.com/interior-api/interior) |
| [Fetch Image Result](actions/fetch-image-result.md) | `POST /v6/images/fetch/{request_id}` | [docs](https://docs.modelslab.com/image-generation/realtime-stable-diffusion/fetchimage) |
| [Fetch Video Result](actions/fetch-video-result.md) | `POST /v6/video/fetch/{request_id}` | [docs](https://docs.modelslab.com/video-api/fetch-video) |
| [Fetch Voice Result](actions/fetch-voice-result.md) | `POST /v6/voice/fetch/{request_id}` | [docs](https://docs.modelslab.com/voice-cloning/fetch-voice) |
| [Generate Face](actions/generate-face.md) | `POST /v6/image_editing/face_gen` | [docs](https://docs.modelslab.com/image-editing/face-gen) |
| [Generate Flux Image](actions/generate-flux-image.md) | `POST /v6/images/text2img` | [docs](https://docs.modelslab.com/image-generation/flux/flux-text-to-image) |
| [Generate Image To Video](actions/generate-image-to-video.md) | `POST /v6/video/img2video` | [docs](https://docs.modelslab.com/video-api/img-to-video) |
| [Generate Image To 3D](actions/generate-image-to3d.md) | `POST /v6/3d/image_to_3d` | [docs](https://docs.modelslab.com/3d-api/image-to-3d) |
| [Generate Realtime Image](actions/generate-realtime-image.md) | `POST /v6/realtime/text2img` | [docs](https://docs.modelslab.com/image-generation/realtime-stable-diffusion/text-to-image) |
| [Generate Sound Effect](actions/generate-sound-effect.md) | `POST /v6/voice/sfx` | [docs](https://docs.modelslab.com/voice-cloning/sfx) |
| [Generate Text To Speech](actions/generate-text-to-speech.md) | `POST /v6/voice/text_to_speech` | [docs](https://docs.modelslab.com/voice-cloning/text-to-speech) |
| [Generate Text To Video](actions/generate-text-to-video.md) | `POST /v6/video/text2video` | [docs](https://docs.modelslab.com/video-api/text-to-video) |
| [Generate Text To 3D](actions/generate-text-to3d.md) | `POST /v6/3d/text_to_3d` | [docs](https://docs.modelslab.com/3d-api/text-to-3d) |
| [Inpaint Image](actions/inpaint-image.md) | `POST /v6/realtime/inpaint` | [docs](https://docs.modelslab.com/image-generation/realtime-stable-diffusion/inpaint) |
| [List Generated Assets](actions/list-generated-assets.md) | `POST /v6/assets_generated` | [docs](https://docs.modelslab.com/general-api/assets-generated) |
| [List Public Models](actions/list-public-models.md) | `POST /v4/dreambooth/model_list` | [docs](https://docs.modelslab.com/image-generation/model-operation/model-list) |
| [List Trained Models](actions/list-trained-models.md) | `POST /v3/finetune_list` | [docs](https://docs.modelslab.com/image-generation/model-operation/finetune-list) |
| [List Uploaded Voices](actions/list-uploaded-voices.md) | `POST /v6/voice/voice_list` | [docs](https://docs.modelslab.com/voice-cloning/voice-list) |
| [Remove Image Background](actions/remove-image-background.md) | `POST /v6/image_editing/removebg_createmask` | [docs](https://docs.modelslab.com/image-editing/removebg-createmask) |
| [Remove Object From Image](actions/remove-object-from-image.md) | `POST /v6/image_editing/object_remover` | [docs](https://docs.modelslab.com/image-editing/object-remover) |
| [Transform Image](actions/transform-image.md) | `POST /v6/realtime/img2img` | [docs](https://docs.modelslab.com/image-generation/realtime-stable-diffusion/image-to-image) |
| [Upscale Image](actions/upscale-image.md) | `POST /v6/image_editing/super_resolution` | [docs](https://docs.modelslab.com/image-editing/super-resolution) |
