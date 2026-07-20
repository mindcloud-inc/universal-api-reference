# Create Image to Video (14B) with PiAPI/Wanx

Creates an image-to-video task in PiAPI/Wanx.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Image to Video (14B)](https://piapi.ai/docs/wanx-api/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | no | Describe the image-to-video motion you want WanX to generate. |
| `input.negative_prompt` | body | `string` | no | Describe elements you want the model to avoid. |
| `input.image` | body | `string` | yes | Image URL or base64 image data for WanX image-to-video generation. |
| `input.aspect_ratio` | body | `string` | no | Supported ratios are 16:9 and 9:16. PiAPI defaults to 16:9. |
