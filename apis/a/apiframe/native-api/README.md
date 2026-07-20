# Apiframe: Native API Reference

A consolidated summary of Apiframe's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.apiframe.ai/
- **API base URL:** `https://api.apiframe.pro`

## Authentication

### API Key

Use your Apiframe API key from the Apiframe dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.apiframe.ai/api-endpoints/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Blend Images](actions/blend-images.md) | `POST /blend` | [docs](https://docs.apiframe.ai/api-endpoints/blend) |
| [Create Image Variations](actions/create-image-variations.md) | `POST /variations` | [docs](https://docs.apiframe.ai/api-endpoints/variations) |
| [Describe Ideogram Image](actions/describe-ideogram-image.md) | `POST /ideogram-describe` | [docs](https://docs.apiframe.ai/ideogram/describe) |
| [Extend Luma Video](actions/extend-luma-video.md) | `POST /luma-extend` | [docs](https://docs.apiframe.ai/luma-ai-api/extend) |
| [Extend Suno Song](actions/extend-suno-song.md) | `POST /suno-extend` | [docs](https://docs.apiframe.ai/suno-ai-api/extend) |
| [Extend Video](actions/extend-video.md) | `POST /imagine-video-extend` | [docs](https://docs.apiframe.ai/api-endpoints/extend-video) |
| [Generate AI Photos](actions/generate-ai-photos.md) | `POST /ai-photo-generate` | [docs](https://docs.apiframe.ai/ai-photos/generate) |
| [Generate Flux Image](actions/generate-flux-image.md) | `POST /flux-imagine` | [docs](https://docs.apiframe.ai/flux/imagine) |
| [Generate Ideogram Image](actions/generate-ideogram-image.md) | `POST /ideogram-imagine` | [docs](https://docs.apiframe.ai/ideogram/imagine) |
| [Generate Image](actions/generate-image.md) | `POST /imagine` | [docs](https://docs.apiframe.ai/api-endpoints/imagine) |
| [Generate Image Prompts](actions/generate-image-prompts.md) | `POST /describe` | [docs](https://docs.apiframe.ai/api-endpoints/describe) |
| [Generate Luma Video](actions/generate-luma-video.md) | `POST /luma-imagine` | [docs](https://docs.apiframe.ai/luma-ai-api/imagine) |
| [Generate Suno Song](actions/generate-suno-song.md) | `POST /suno-imagine` | [docs](https://docs.apiframe.ai/suno-ai-api/imagine) |
| [Generate Udio Song](actions/generate-udio-song.md) | `POST /udio-generate` | [docs](https://docs.apiframe.ai/udio-ai-api/generate-a-song) |
| [Generate Video](actions/generate-video.md) | `POST /imagine-video` | [docs](https://docs.apiframe.ai/api-endpoints/imagine-video) |
| [Get Account Info](actions/get-account-info.md) | `GET /account` | [docs](https://docs.apiframe.ai/api-endpoints/account-info) |
| [Get Image Seed](actions/get-image-seed.md) | `POST /seed` | [docs](https://docs.apiframe.ai/api-endpoints/seed) |
| [Get Task Result](actions/get-task-result.md) | `POST /fetch` | [docs](https://docs.apiframe.ai/api-endpoints/fetch) |
| [Get Task Results](actions/get-task-results.md) | `POST /fetch-many` | [docs](https://docs.apiframe.ai/api-endpoints/fetch-many) |
| [Outpaint Image](actions/outpaint-image.md) | `POST /outpaint` | [docs](https://docs.apiframe.ai/api-endpoints/outpaint-zoom-out) |
| [Pan Image](actions/pan-image.md) | `POST /pan` | [docs](https://docs.apiframe.ai/api-endpoints/pan) |
| [Redraw Image Region](actions/redraw-image-region.md) | `POST /inpaint` | [docs](https://docs.apiframe.ai/api-endpoints/inpaint-vary-region) |
| [Remix Ideogram Image](actions/remix-ideogram-image.md) | `POST /ideogram-remix` | [docs](https://docs.apiframe.ai/ideogram/remix) |
| [Reroll Images](actions/reroll-images.md) | `POST /reroll` | [docs](https://docs.apiframe.ai/api-endpoints/reroll) |
| [Swap Face](actions/swap-face.md) | `POST /faceswap` | [docs](https://docs.apiframe.ai/api-endpoints/faceswap) |
| [Train AI Photo Model](actions/train-ai-photo-model.md) | `POST /ai-photo-train` | [docs](https://docs.apiframe.ai/ai-photos/train) |
| [Upload and Prepare Training Images](actions/upload-and-prepare-training-images.md) | `POST /ai-photo-upload` | [docs](https://docs.apiframe.ai/ai-photos/upload-and-prepare) |
| [Upload Audio](actions/upload-audio.md) | `POST /suno-upload` | [docs](https://docs.apiframe.ai/suno-ai-api/upload) |
| [Upload Image](actions/upload-image.md) | `POST /upload` | [docs](https://docs.apiframe.ai/media-upload-apis/upload-image) |
| [Upscale Ideogram Image](actions/upscale-ideogram-image.md) | `POST /ideogram-upscale` | [docs](https://docs.apiframe.ai/ideogram/upscale) |
