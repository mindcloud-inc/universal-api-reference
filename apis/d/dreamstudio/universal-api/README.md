# <img src="https://images.mindcloud.co/apps/icons/dreamstudio_1776427026663.png" alt="Dreamstudio logo" width="28" height="28"> Dreamstudio: Universal API

Generate, edit, upscale, and transform images, audio, and 3D assets with Stability AI's DreamStudio API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dreamstudio/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://platform.stability.ai
- **Vendor API docs:** https://platform.stability.ai/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credit Balance](actions/get-credit-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Credit Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Balance](actions/get-credit-balance.md) | GET | Retrieves account credit balance from Dreamstudio. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Audio to Audio](actions/audio-to-audio.md) | POST | Creates audio from an audio sample in Dreamstudio. |
| [Conservative Upscale](actions/conservative-upscale.md) | POST | Creates a conservative 4K upscale in Dreamstudio. |
| [Creative Upscale](actions/creative-upscale.md) | POST | Creates a creative upscale job in Dreamstudio. |
| [Erase Objects](actions/erase-objects.md) | PUT | Removes masked objects from an image in Dreamstudio. |
| [Fast Upscale](actions/fast-upscale.md) | POST | Creates a fast 4x upscale in Dreamstudio. |
| [Fetch Async Result](actions/fetch-async-result.md) | GET | Retrieves an async generation result from Dreamstudio. |
| [Generate Image from Image (Legacy)](actions/generate-image-from-image-legacy.md) | POST | Creates a legacy image-to-image result in Dreamstudio. |
| [Generate Point-Aware 3D Model](actions/generate-point-aware3d-model.md) | POST | Creates a point-aware 3D model in Dreamstudio. |
| [Generate 3D Model](actions/generate3d-model.md) | POST | Creates a 3D model from an image in Dreamstudio. |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves authenticated account details from Dreamstudio. |
| [Get Creative Upscale Result](actions/get-creative-upscale-result.md) | GET | Retrieves a creative upscale result from Dreamstudio. |
| [Get Legacy Upscale Result](actions/get-legacy-upscale-result.md) | GET | Retrieves a legacy upscale result from Dreamstudio. |
| [Inpaint Audio](actions/inpaint-audio.md) | POST | Creates inpainted audio from a sample in Dreamstudio. |
| [Inpaint Image](actions/inpaint-image.md) | PUT | Fills masked regions in an image in Dreamstudio. |
| [Legacy Inpaint Image](actions/legacy-inpaint-image.md) | POST | Creates a legacy inpainted image in Dreamstudio. |
| [Legacy Upscale Image](actions/legacy-upscale-image.md) | POST | Creates a legacy upscale job in Dreamstudio. |
| [List Available Engines](actions/list-available-engines.md) | GET | Retrieves available generation engines from Dreamstudio. |
| [Outpaint Image](actions/outpaint-image.md) | PUT | Expands an image beyond its borders in Dreamstudio. |
| [Remove Background](actions/remove-background.md) | PUT | Removes the background from an image in Dreamstudio. |
| [Replace Background and Relight](actions/replace-background-and-relight.md) | PUT | Replaces an image background and relights it in Dreamstudio. |
| [Search and Recolor](actions/search-and-recolor.md) | PUT | Recolors a selected object in an image in Dreamstudio. |
| [Search and Replace](actions/search-and-replace.md) | PUT | Replaces a selected object in an image in Dreamstudio. |
| [Sketch Control](actions/sketch-control.md) | POST | Creates an image from a sketch in Dreamstudio. |
| [Stable Diffusion 3.5](actions/stable-diffusion35.md) | POST | Creates an image with Stable Diffusion 3.5 in Dreamstudio. |
| [Stable Image Core](actions/stable-image-core.md) | POST | Creates an image with Stable Image Core in Dreamstudio. |
| [Stable Image Ultra](actions/stable-image-ultra.md) | POST | Creates an image with Stable Image Ultra in Dreamstudio. |
| [Structure Control](actions/structure-control.md) | POST | Creates an image from a reference structure in Dreamstudio. |
| [Style Guide Control](actions/style-guide-control.md) | POST | Creates an image using a style guide in Dreamstudio. |
| [Style Transfer](actions/style-transfer.md) | POST | Applies reference image styles to an image in Dreamstudio. |
| [Text to Audio](actions/text-to-audio.md) | POST | Creates audio from a text prompt in Dreamstudio. |

