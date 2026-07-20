# <img src="https://images.mindcloud.co/apps/icons/stability-ai-icon-square_1775848806894.png" alt="Stable Diffusion logo" width="28" height="28"> Stable Diffusion: Universal API

Generate, edit, upscale, control, and retrieve AI media outputs across Stability AI image, audio, 3D, and async result APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stableDiffusion/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://stability.ai
- **Vendor API docs:** https://platform.stability.ai/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Balance](actions/get-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from Stable Diffusion. |

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves account balance from Stable Diffusion. |

### Engine

| Action | Method | Description |
| --- | --- | --- |
| [List Engines](actions/list-engines.md) | GET | Retrieves available engines from Stable Diffusion. |

### Stableaudiogeneration

| Action | Method | Description |
| --- | --- | --- |
| [Generate Audio From Text](actions/generate-audio-from-text.md) | POST | Generates audio from text in Stable Diffusion. |
| [Inpaint Audio](actions/inpaint-audio.md) | POST | Inpaints audio in Stable Diffusion. |
| [Transform Audio From Audio](actions/transform-audio-from-audio.md) | POST | Transforms audio from an input clip in Stable Diffusion. |

### Stablegenerationresult

| Action | Method | Description |
| --- | --- | --- |
| [Get Generation Result](actions/get-generation-result.md) | GET | Retrieves a generation result from Stable Diffusion. |

### Stableimagecontrol

| Action | Method | Description |
| --- | --- | --- |
| [Control Sketch Image](actions/control-sketch-image.md) | POST | Generates an image from a sketch in Stable Diffusion. |
| [Control Structure Image](actions/control-structure-image.md) | POST | Generates an image from structure guidance in Stable Diffusion. |
| [Control Style Image](actions/control-style-image.md) | POST | Generates an image from style guidance in Stable Diffusion. |
| [Transfer Style Image](actions/transfer-style-image.md) | POST | Transfers image style in Stable Diffusion. |

### Stableimageedit

| Action | Method | Description |
| --- | --- | --- |
| [Erase Image Region](actions/erase-image-region.md) | POST | Erases a region from an image in Stable Diffusion. |
| [Inpaint Image](actions/inpaint-image.md) | POST | Inpaints an image in Stable Diffusion. |
| [Inpaint Legacy Image](actions/inpaint-legacy-image.md) | POST | Inpaints an image with the legacy Stable Diffusion endpoint. |
| [Mask XL Image](actions/mask-xl-image.md) | POST | Masks an XL image in Stable Diffusion. |
| [Outpaint Image](actions/outpaint-image.md) | POST | Outpaints an image in Stable Diffusion. |
| [Remove Background](actions/remove-background.md) | POST | Removes an image background in Stable Diffusion. |
| [Replace Background And Relight](actions/replace-background-and-relight.md) | POST | Replaces an image background and relights the subject in Stable Diffusion. |
| [Search And Recolor](actions/search-and-recolor.md) | POST | Recolors matched content in an image in Stable Diffusion. |
| [Search And Replace](actions/search-and-replace.md) | POST | Replaces matched content in an image in Stable Diffusion. |
| [Transform XL Image](actions/transform-xl-image.md) | POST | Transforms an XL image in Stable Diffusion. |

### Stableimagegeneration

| Action | Method | Description |
| --- | --- | --- |
| [Generate Core Image](actions/generate-core-image.md) | POST | Generates an image with Stable Diffusion Core. |
| [Generate SD3 Image](actions/generate-sd3-image.md) | POST | Generates an image with Stable Diffusion SD3. |
| [Generate Ultra Image](actions/generate-ultra-image.md) | POST | Generates an image with Stable Diffusion Ultra. |
| [Generate XL Image](actions/generate-xl-image.md) | POST | Generates an XL image in Stable Diffusion. |

### Stableimageupscale

| Action | Method | Description |
| --- | --- | --- |
| [Get Async Upscale Result](actions/get-async-upscale-result.md) | GET | Retrieves an asynchronous upscale result from Stable Diffusion. |
| [Get Creative Upscale Result](actions/get-creative-upscale-result.md) | GET | Retrieves a creative upscale result from Stable Diffusion. |
| [Submit Async Upscale](actions/submit-async-upscale.md) | POST | Submits an asynchronous upscale request to Stable Diffusion. |
| [Upscale Image Conservative](actions/upscale-image-conservative.md) | POST | Upscales an image with Stable Diffusion Conservative. |
| [Upscale Image Creative](actions/upscale-image-creative.md) | POST | Upscales an image creatively in Stable Diffusion. |
| [Upscale Image Fast](actions/upscale-image-fast.md) | POST | Upscales an image with Stable Diffusion Fast. |

