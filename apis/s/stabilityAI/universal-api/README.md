# <img src="https://images.mindcloud.co/apps/icons/stability-ai-icon_1778187995942.png" alt="Stability AI logo" width="28" height="28"> Stability AI: Universal API

Generate and edit images, audio, and 3D assets with Stability AI's REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stabilityAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://stability.ai
- **Vendor API docs:** https://platform.stability.ai/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Fetch Async Generation Result](actions/fetch-async-generation-result.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/fetch-async-generation-result?connectionId=$CONNECTION_ID&id=generation-result-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### 3d Asset

| Action | Method | Description |
| --- | --- | --- |
| [Generate Fast 3D Asset](actions/generate-fast3-d-asset.md) | POST | Creates a 3D asset in Stability AI from one image. |
| [Generate Point Aware 3D Asset](actions/generate-point-aware3-d-asset.md) | POST | Creates a point-aware 3D asset in Stability AI. |

### Async Relight Job

| Action | Method | Description |
| --- | --- | --- |
| [Replace Background And Relight](actions/replace-background-and-relight.md) | PUT | Updates an image in Stability AI with background replacement. |

### Async Upscale Job

| Action | Method | Description |
| --- | --- | --- |
| [Creative Upscale Image](actions/creative-upscale-image.md) | POST | Upscales an image in Stability AI with creative mode. |

### Audio

| Action | Method | Description |
| --- | --- | --- |
| [Generate Audio From Audio](actions/generate-audio-from-audio.md) | POST | Creates audio in Stability AI from an audio sample. |
| [Generate Audio From Text](actions/generate-audio-from-text.md) | POST | Creates audio in Stability AI from a text prompt. |
| [Inpaint Audio](actions/inpaint-audio.md) | PUT | Updates audio in Stability AI with inpainting. |

### Creative Upscale Result

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Creative Upscale Result](actions/fetch-creative-upscale-result.md) | GET | Retrieves a creative upscale result from Stability AI. |

### Generation Result

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Async Generation Result](actions/fetch-async-generation-result.md) | GET | Retrieves an asynchronous generation result from Stability AI. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Conservative Upscale Image](actions/conservative-upscale-image.md) | POST | Upscales an image in Stability AI with conservative mode. |
| [Control Sketch Image](actions/control-sketch-image.md) | POST | Creates an image in Stability AI from a sketch. |
| [Control Structure Image](actions/control-structure-image.md) | POST | Creates an image in Stability AI from image structure. |
| [Control Style Image](actions/control-style-image.md) | POST | Creates an image in Stability AI from a style guide. |
| [Fast Upscale Image](actions/fast-upscale-image.md) | POST | Upscales an image in Stability AI with fast mode. |
| [Generate Image Core](actions/generate-image-core.md) | POST | Creates an image in Stability AI with Core. |
| [Generate Image SD3](actions/generate-image-sd3.md) | POST | Creates an image in Stability AI with SD3. |
| [Generate Image Ultra](actions/generate-image-ultra.md) | POST | Creates an image in Stability AI with Ultra. |
| [Inpaint Image](actions/inpaint-image.md) | PUT | Updates an image in Stability AI with inpainting. |
| [Outpaint Image](actions/outpaint-image.md) | PUT | Updates an image in Stability AI with outpainting. |
| [Remove Image Background](actions/remove-image-background.md) | POST | Removes an image background in Stability AI. |
| [Search And Recolor Image](actions/search-and-recolor-image.md) | PUT | Updates an image in Stability AI by search and recolor. |
| [Search And Replace Image](actions/search-and-replace-image.md) | PUT | Updates an image in Stability AI by search and replace. |
| [Transfer Image Style](actions/transfer-image-style.md) | PUT | Updates an image in Stability AI with style transfer. |

