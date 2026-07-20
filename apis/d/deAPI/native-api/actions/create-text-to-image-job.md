# Create Text-to-Image Job with deAPI

Creates a text-to-image job in deAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/client/txt2img`
- **Base URL:** `https://api.deapi.ai`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guidance` | body | `string` | no | Guidance scale for generation. |
| `height` | body | `string` | no | Image height in pixels. |
| `model` | body | `string` | no | Image model slug from List Models. |
| `negative_prompt` | body | `string` | no | Elements to avoid in the generated image. |
| `prompt` | body | `string` | no | Main prompt for image generation. |
| `seed` | body | `string` | no | Random seed for generation. |
| `steps` | body | `string` | no | Number of inference steps. |
| `width` | body | `string` | no | Image width in pixels. |
