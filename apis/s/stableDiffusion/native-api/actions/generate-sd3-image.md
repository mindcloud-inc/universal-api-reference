# Generate SD3 Image with Stable Diffusion

Generates an image with Stable Diffusion SD3.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/generate/sd3`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Generate SD3 Image](https://platform.stability.ai/docs/api-reference#tag/Generate/paths/~1v2beta~1stable-image~1generate~1sd3/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt describing the image to generate. |
