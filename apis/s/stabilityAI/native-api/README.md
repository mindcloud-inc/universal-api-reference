# Stability AI: Native API Reference

A consolidated summary of Stability AI's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://platform.stability.ai/docs/api-reference
- **OpenAPI specification:** https://api.stability.ai/v2alpha/openapi
- **API base URL:** `https://api.stability.ai`

## Authentication

### Stability API Key

Authenticate requests with a Stability API key in the Authorization bearer header.

### Credentials

- **Stability API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://platform.stability.ai/docs/api-reference)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Conservative Upscale Image](actions/conservative-upscale-image.md) | `POST /v2beta/stable-image/upscale/conservative` | [docs](https://platform.stability.ai/docs/api-reference#tag/Upscale/paths/~1v2beta~1stable-image~1upscale~1conservative/post) |
| [Control Sketch Image](actions/control-sketch-image.md) | `POST /v2beta/stable-image/control/sketch` | [docs](https://platform.stability.ai/docs/api-reference#tag/Control/paths/~1v2beta~1stable-image~1control~1sketch/post) |
| [Control Structure Image](actions/control-structure-image.md) | `POST /v2beta/stable-image/control/structure` | [docs](https://platform.stability.ai/docs/api-reference#tag/Control/paths/~1v2beta~1stable-image~1control~1structure/post) |
| [Control Style Image](actions/control-style-image.md) | `POST /v2beta/stable-image/control/style` | [docs](https://platform.stability.ai/docs/api-reference#tag/Control/paths/~1v2beta~1stable-image~1control~1style/post) |
| [Creative Upscale Image](actions/creative-upscale-image.md) | `POST /v2beta/stable-image/upscale/creative` | [docs](https://platform.stability.ai/docs/api-reference#tag/Upscale/paths/~1v2beta~1stable-image~1upscale~1creative/post) |
| [Fast Upscale Image](actions/fast-upscale-image.md) | `POST /v2beta/stable-image/upscale/fast` | [docs](https://platform.stability.ai/docs/api-reference#tag/Upscale/paths/~1v2beta~1stable-image~1upscale~1fast/post) |
| [Fetch Async Generation Result](actions/fetch-async-generation-result.md) | `GET /v2beta/results/[:id]` | [docs](https://platform.stability.ai/docs/api-reference#tag/Results/paths/~1v2beta~1results~1{id}/get) |
| [Fetch Creative Upscale Result](actions/fetch-creative-upscale-result.md) | `GET /v2beta/stable-image/upscale/creative/result/[:id]` | [docs](https://platform.stability.ai/docs/api-reference#tag/Upscale/paths/~1v2beta~1stable-image~1upscale~1creative~1result~1{id}/get) |
| [Generate Audio From Audio](actions/generate-audio-from-audio.md) | `POST /v2beta/audio/stable-audio-2/audio-to-audio` | [docs](https://platform.stability.ai/docs/api-reference#tag/Stable-Audio-2/paths/~1v2beta~1audio~1stable-audio-2~1audio-to-audio/post) |
| [Generate Audio From Text](actions/generate-audio-from-text.md) | `POST /v2beta/audio/stable-audio-2/text-to-audio` | [docs](https://platform.stability.ai/docs/api-reference#tag/Stable-Audio-2/paths/~1v2beta~1audio~1stable-audio-2~1text-to-audio/post) |
| [Generate Fast 3D Asset](actions/generate-fast3-d-asset.md) | `POST /v2beta/3d/stable-fast-3d` | [docs](https://platform.stability.ai/docs/api-reference#tag/3D/paths/~1v2beta~13d~1stable-fast-3d/post) |
| [Generate Image Core](actions/generate-image-core.md) | `POST /v2beta/stable-image/generate/core` | [docs](https://platform.stability.ai/docs/api-reference#tag/Generate/paths/~1v2beta~1stable-image~1generate~1core/post) |
| [Generate Image SD3](actions/generate-image-sd3.md) | `POST /v2beta/stable-image/generate/sd3` | [docs](https://platform.stability.ai/docs/api-reference#tag/Generate/paths/~1v2beta~1stable-image~1generate~1sd3/post) |
| [Generate Image Ultra](actions/generate-image-ultra.md) | `POST /v2beta/stable-image/generate/ultra` | [docs](https://platform.stability.ai/docs/api-reference#tag/Generate/paths/~1v2beta~1stable-image~1generate~1ultra/post) |
| [Generate Point Aware 3D Asset](actions/generate-point-aware3-d-asset.md) | `POST /v2beta/3d/stable-point-aware-3d` | [docs](https://platform.stability.ai/docs/api-reference#tag/3D/paths/~1v2beta~13d~1stable-point-aware-3d/post) |
| [Inpaint Audio](actions/inpaint-audio.md) | `POST /v2beta/audio/stable-audio-2/inpaint` | [docs](https://platform.stability.ai/docs/api-reference#tag/Stable-Audio-2/paths/~1v2beta~1audio~1stable-audio-2~1inpaint/post) |
| [Inpaint Image](actions/inpaint-image.md) | `POST /v2beta/stable-image/edit/inpaint` | [docs](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1inpaint/post) |
| [Outpaint Image](actions/outpaint-image.md) | `POST /v2beta/stable-image/edit/outpaint` | [docs](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1outpaint/post) |
| [Remove Image Background](actions/remove-image-background.md) | `POST /v2beta/stable-image/edit/remove-background` | [docs](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1remove-background/post) |
| [Replace Background And Relight](actions/replace-background-and-relight.md) | `POST /v2beta/stable-image/edit/replace-background-and-relight` | [docs](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1replace-background-and-relight/post) |
| [Search And Recolor Image](actions/search-and-recolor-image.md) | `POST /v2beta/stable-image/edit/search-and-recolor` | [docs](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1search-and-recolor/post) |
| [Search And Replace Image](actions/search-and-replace-image.md) | `POST /v2beta/stable-image/edit/search-and-replace` | [docs](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1search-and-replace/post) |
| [Transfer Image Style](actions/transfer-image-style.md) | `POST /v2beta/stable-image/control/style-transfer` | [docs](https://platform.stability.ai/docs/api-reference#tag/Control/paths/~1v2beta~1stable-image~1control~1style-transfer/post) |
