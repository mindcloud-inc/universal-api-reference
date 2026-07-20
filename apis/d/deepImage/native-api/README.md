# DeepImage: Native API Reference

A consolidated summary of DeepImage's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://documentation.deep-image.ai/
- **API base URL:** `https://deep-image.ai`

## Authentication

### API Key

Authenticate with your DeepImage API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://documentation.deep-image.ai/quick-start)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accurate Business Avatar](actions/accurate-business-avatar.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/common-usecases/create-business-photo-or-avatar-from-face-image) |
| [Add Caption Overlay](actions/add-caption-overlay.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/captions) |
| [Auto Enhance Flux2 Klein 9B](actions/auto-enhance-flux2-klein9b.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/common-usecases/auto-enhance-image-quality) |
| [Auto Enhance Generative](actions/auto-enhance-generative.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/common-usecases/auto-enhance-image-quality) |
| [Auto Enhance Image Quality](actions/auto-enhance-image-quality.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/common-usecases/auto-enhance-image-quality) |
| [Auto Enhance Pro](actions/auto-enhance-pro.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/common-usecases/auto-enhance-image-quality) |
| [Auto Enhance Qwen](actions/auto-enhance-qwen.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/common-usecases/auto-enhance-image-quality) |
| [Business Avatar Generation](actions/business-avatar-generation.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/common-usecases/create-business-photo-or-avatar-from-face-image) |
| [Clean Image Artifacts](actions/clean-image-artifacts.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/denoise-and-sharpen) |
| [Correct Exposure](actions/correct-exposure.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/enhance-lighting-and-colors) |
| [Correct White Balance](actions/correct-white-balance.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/enhance-lighting-and-colors) |
| [Deblur Image](actions/deblur-image.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/denoise-and-sharpen) |
| [Delete Completed Job](actions/delete-completed-job.md) | `DELETE /rest_api/result/:hash` | [docs](https://documentation.deep-image.ai/api-methods) |
| [Denoise Image](actions/denoise-image.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/denoise-and-sharpen) |
| [Doodle to Image](actions/doodle-to-image.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/common-usecases/ai-drawing-to-image-doodle) |
| [Enhance Colors](actions/enhance-colors.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/enhance-lighting-and-colors) |
| [Enhance Face Details](actions/enhance-face-details.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/enhance-face-details) |
| [Enhance Lighting](actions/enhance-lighting.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/enhance-lighting-and-colors) |
| [Face Swap](actions/face-swap.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/common-usecases/face-swap) |
| [Generate Product Scene (Blended)](actions/generate-product-scene-blended.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/common-usecases/create-beautiful-product-photo) |
| [Generate Product Scene (Fully Generative)](actions/generate-product-scene-fully-generative.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/common-usecases/create-beautiful-product-photo) |
| [Generative Upscale](actions/generative-upscale.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/common-usecases/genarate-image-in-high-resolution) |
| [Get Account Info](actions/get-account-info.md) | `GET /rest_api/me` | [docs](https://documentation.deep-image.ai/account-and-settings/account-information) |
| [Get Processing Job Result](actions/get-processing-job-result.md) | `GET /rest_api/result/:hash` | [docs](https://documentation.deep-image.ai/account-and-settings/account-information) |
| [Inpainting / Outpainting](actions/inpainting-outpainting.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/image-processing/inpainting-and-outpainting-uncrop) |
| [Prepare for Print](actions/prepare-for-print.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/print) |
| [Process Image and Return Result](actions/process-image-and-return-result.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/api-methods) |
| [Product Photo Unification](actions/product-photo-unification.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/common-usecases/product-photo-unification) |
| [Prompt-Based Image Editing](actions/prompt-based-image-editing.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/image-processing/prompt-based-image-editing) |
| [Queue Image Processing Job](actions/queue-image-processing-job.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/api-methods) |
| [Remove Background (Auto)](actions/remove-background-auto.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/background-removal-and-generation) |
| [Remove Background (Human)](actions/remove-background-human.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/background-removal-and-generation) |
| [Remove Background (Item)](actions/remove-background-item.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/background-removal-and-generation) |
| [Replace Background with Backdrop Image](actions/replace-background-with-backdrop-image.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/background-removal-and-generation) |
| [Replace Background with Solid Color](actions/replace-background-with-solid-color.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/background-removal-and-generation) |
| [Resize to Exact Dimensions](actions/resize-to-exact-dimensions.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/resize-and-padding) |
| [Smart Content Crop](actions/smart-content-crop.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/frame-identification) |
| [Storage-to-Storage Processing](actions/storage-to-storage-processing.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/storages/usage) |
| [Text-to-Image Generation](actions/text-to-image-generation.md) | `POST /rest_api/process` | [docs](https://documentation.deep-image.ai/image-processing/image-generation) |
| [Upscale by Percentage](actions/upscale-by-percentage.md) | `POST /rest_api/process_result` | [docs](https://documentation.deep-image.ai/image-processing/resize-and-padding) |
