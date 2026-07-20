# Create Text-to-Music Job with deAPI

Creates a text-to-music job in deAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/client/txt2music`
- **Base URL:** `https://api.deapi.ai`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caption` | body | `string` | no | Text description of the music to generate. |
| `duration` | body | `string` | no | Music duration in seconds. |
| `format` | body | `string` | no | Audio output format. |
| `guidance_scale` | body | `string` | no | Classifier-free guidance scale. |
| `inference_steps` | body | `string` | no | Number of diffusion inference steps. |
| `lyrics` | body | `string` | no | Lyrics text, or [Instrumental] for instrumental output. |
| `model` | body | `string` | no | Music model slug from List Models. |
| `seed` | body | `string` | no | Random seed. Use -1 for random. |
