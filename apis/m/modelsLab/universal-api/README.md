# <img src="https://images.mindcloud.co/apps/icons/models-lab_1778005652684.png" alt="ModelsLab logo" width="28" height="28"> ModelsLab: Universal API

ModelsLab provides AI APIs for image generation, video generation, audio and voice workflows, 3D generation, image editing, and related account utilities.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/modelsLab/latest
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://modelslab.com
- **Vendor API docs:** https://docs.modelslab.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Processing Requests](actions/check-processing-requests.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/check-processing-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### 3d Asset

| Action | Method | Description |
| --- | --- | --- |
| [Generate Text To 3D](actions/generate-text-to3d.md) | POST | Creates a 3D asset from text in ModelsLab. |

### Background Removal

| Action | Method | Description |
| --- | --- | --- |
| [Remove Image Background](actions/remove-image-background.md) | POST | Creates a background-removed image in ModelsLab. |

### Face Generation

| Action | Method | Description |
| --- | --- | --- |
| [Generate Face](actions/generate-face.md) | POST | Creates a generated face image in ModelsLab. |

### Flux Image Generation

| Action | Method | Description |
| --- | --- | --- |
| [Generate Flux Image](actions/generate-flux-image.md) | POST | Creates a Flux image in ModelsLab. |

### Generated Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Generated Assets](actions/list-generated-assets.md) | GET | Retrieves generated assets from ModelsLab. |

### Image Caption

| Action | Method | Description |
| --- | --- | --- |
| [Caption Image](actions/caption-image.md) | POST | Creates an image caption in ModelsLab. |

### Image Generation

| Action | Method | Description |
| --- | --- | --- |
| [Generate Realtime Image](actions/generate-realtime-image.md) | POST | Creates a realtime image in ModelsLab. |

### Image Generation Result

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Image Result](actions/fetch-image-result.md) | GET | Retrieves a generated image result from ModelsLab. |

### Image Inpaint

| Action | Method | Description |
| --- | --- | --- |
| [Inpaint Image](actions/inpaint-image.md) | POST | Creates an inpainted image in ModelsLab. |

### Image To 3d Asset

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image To 3D](actions/generate-image-to3d.md) | POST | Creates a 3D asset from an image in ModelsLab. |

### Image To Video Generation

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image To Video](actions/generate-image-to-video.md) | POST | Creates a video from an image in ModelsLab. |

### Image Transformation

| Action | Method | Description |
| --- | --- | --- |
| [Transform Image](actions/transform-image.md) | POST | Creates a transformed image in ModelsLab. |

### Image Upscale

| Action | Method | Description |
| --- | --- | --- |
| [Upscale Image](actions/upscale-image.md) | POST | Creates an upscaled image in ModelsLab. |

### Interior Design

| Action | Method | Description |
| --- | --- | --- |
| [Design Interior](actions/design-interior.md) | POST | Creates an interior design image in ModelsLab. |

### Object Removal

| Action | Method | Description |
| --- | --- | --- |
| [Remove Object From Image](actions/remove-object-from-image.md) | POST | Creates an object-removed image in ModelsLab. |

### Processing Request Count

| Action | Method | Description |
| --- | --- | --- |
| [Check Processing Requests](actions/check-processing-requests.md) | GET | Retrieves processing request counts from ModelsLab. |

### Prompt Safety Check

| Action | Method | Description |
| --- | --- | --- |
| [Check Prompt Safety](actions/check-prompt-safety.md) | GET | Checks a prompt for safety issues in ModelsLab. |

### Public Model

| Action | Method | Description |
| --- | --- | --- |
| [List Public Models](actions/list-public-models.md) | GET | Retrieves public models from ModelsLab. |

### Sound Effect

| Action | Method | Description |
| --- | --- | --- |
| [Generate Sound Effect](actions/generate-sound-effect.md) | POST | Creates a sound effect in ModelsLab. |

### Speech Audio

| Action | Method | Description |
| --- | --- | --- |
| [Generate Text To Speech](actions/generate-text-to-speech.md) | POST | Creates speech audio from text in ModelsLab. |

### Trained Model

| Action | Method | Description |
| --- | --- | --- |
| [List Trained Models](actions/list-trained-models.md) | GET | Retrieves trained models from ModelsLab. |

### Video Generation

| Action | Method | Description |
| --- | --- | --- |
| [Generate Text To Video](actions/generate-text-to-video.md) | POST | Creates a video from text in ModelsLab. |

### Video Generation Result

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Video Result](actions/fetch-video-result.md) | GET | Retrieves a generated video result from ModelsLab. |

### Voice

| Action | Method | Description |
| --- | --- | --- |
| [List Uploaded Voices](actions/list-uploaded-voices.md) | GET | Retrieves uploaded voices from ModelsLab. |

### Voice Generation Result

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Voice Result](actions/fetch-voice-result.md) | GET | Retrieves a generated voice result from ModelsLab. |

