# Dreamstudio: Native API Reference

A consolidated summary of Dreamstudio's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://platform.stability.ai/docs/api-reference
- **OpenAPI specification:** https://api.stability.ai/v2alpha/openapi
- **API base URL:** `https://api.stability.ai`

## Authentication

### API Key

Authenticate to Stability AI with a DreamStudio API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://platform.stability.ai/docs/getting-started/authentication)

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Audio to Audio](actions/audio-to-audio.md) | `POST /v2beta/audio/stable-audio-2/audio-to-audio` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Conservative Upscale](actions/conservative-upscale.md) | `POST /v2beta/stable-image/upscale/conservative` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Creative Upscale](actions/creative-upscale.md) | `POST /v2beta/stable-image/upscale/creative` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Erase Objects](actions/erase-objects.md) | `POST /v2beta/stable-image/edit/erase` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Fast Upscale](actions/fast-upscale.md) | `POST /v2beta/stable-image/upscale/fast` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Fetch Async Result](actions/fetch-async-result.md) | `GET /v2beta/results/:id` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Generate Image from Image (Legacy)](actions/generate-image-from-image-legacy.md) | `POST /v1/generation/:engine_id/image-to-image` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Generate Point-Aware 3D Model](actions/generate-point-aware3d-model.md) | `POST /v2beta/3d/stable-point-aware-3d` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Generate 3D Model](actions/generate3d-model.md) | `POST /v2beta/3d/stable-fast-3d` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Get Account Details](actions/get-account-details.md) | `GET /v1/user/account` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Get Creative Upscale Result](actions/get-creative-upscale-result.md) | `GET /v2beta/stable-image/upscale/creative/result/:id` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Get Credit Balance](actions/get-credit-balance.md) | `GET /v1/user/balance` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Get Legacy Upscale Result](actions/get-legacy-upscale-result.md) | `GET /v2alpha/generation/stable-image/upscale/result/:id` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Inpaint Audio](actions/inpaint-audio.md) | `POST /v2beta/audio/stable-audio-2/inpaint` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Inpaint Image](actions/inpaint-image.md) | `POST /v2beta/stable-image/edit/inpaint` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Legacy Inpaint Image](actions/legacy-inpaint-image.md) | `POST /v2alpha/generation/stable-image/inpaint` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Legacy Upscale Image](actions/legacy-upscale-image.md) | `POST /v2alpha/generation/stable-image/upscale` | [docs](https://platform.stability.ai/docs/api-reference) |
| [List Available Engines](actions/list-available-engines.md) | `GET /v1/engines/list` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Outpaint Image](actions/outpaint-image.md) | `POST /v2beta/stable-image/edit/outpaint` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Remove Background](actions/remove-background.md) | `POST /v2beta/stable-image/edit/remove-background` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Replace Background and Relight](actions/replace-background-and-relight.md) | `POST /v2beta/stable-image/edit/replace-background-and-relight` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Search and Recolor](actions/search-and-recolor.md) | `POST /v2beta/stable-image/edit/search-and-recolor` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Search and Replace](actions/search-and-replace.md) | `POST /v2beta/stable-image/edit/search-and-replace` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Sketch Control](actions/sketch-control.md) | `POST /v2beta/stable-image/control/sketch` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Stable Diffusion 3.5](actions/stable-diffusion35.md) | `POST /v2beta/stable-image/generate/sd3` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Stable Image Core](actions/stable-image-core.md) | `POST /v2beta/stable-image/generate/core` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Stable Image Ultra](actions/stable-image-ultra.md) | `POST /v2beta/stable-image/generate/ultra` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Structure Control](actions/structure-control.md) | `POST /v2beta/stable-image/control/structure` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Style Guide Control](actions/style-guide-control.md) | `POST /v2beta/stable-image/control/style` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Style Transfer](actions/style-transfer.md) | `POST /v2beta/stable-image/control/style-transfer` | [docs](https://platform.stability.ai/docs/api-reference) |
| [Text to Audio](actions/text-to-audio.md) | `POST /v2beta/audio/stable-audio-2/text-to-audio` | [docs](https://platform.stability.ai/docs/api-reference) |
