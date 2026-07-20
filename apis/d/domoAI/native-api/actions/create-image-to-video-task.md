# Create Image to Video Task with DomoAI

Creates a new image-to-video task in DomoAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/video/image2video`
- **Base URL:** `https://api.domoai.com`
- **Official documentation:** [Create Image to Video Task](https://docs.domoai.app/api-reference/ai-video/image-to-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `list` | yes | The DomoAI image-to-video model version. Accepted values: `animate-2.4-advanced`, `animate-2.4-faster`. |
| `image.domoai_uri` | body | `string` | yes | A domoai_uri from the Upload File action. |
| `image.bytes_base64_encoded` | body | `string` | no | Base64-encoded image bytes. |
| `seconds` | body | `number` | yes | Output video duration in seconds. |
| `prompt` | body | `string` | no | Optional text prompt describing the video style or motion. |
| `aspect_ratio` | body | `list` | no | Output video aspect ratio. Accepted values: `16:9`, `1:1`, `3:4`, `4:3`, `9:16`. |
| `callback_url` | body | `string` | no | Optional URL that DomoAI should notify when task status changes. |
