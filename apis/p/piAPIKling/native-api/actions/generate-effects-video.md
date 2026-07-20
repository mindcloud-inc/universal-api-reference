# Generate Effects Video with PiAPI/Kling

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Generate Effects Video](https://piapi.ai/docs/kling-api/kling-effects-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.image_url` | body | `string` | yes | Source image URL for the effects video. |
| `input.effect` | body | `string` | yes | Effect name such as squish, kissing, hugging, or fighting. |
| `input.prompt` | body | `string` | yes | Describe how the effect should play out in the scene. |
| `input.professional_mode` | body | `boolean` | no | Use the higher-cost professional effects mode. |
