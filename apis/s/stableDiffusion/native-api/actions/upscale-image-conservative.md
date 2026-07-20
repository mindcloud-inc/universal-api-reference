# Upscale Image Conservative with Stable Diffusion

Upscales an image with Stable Diffusion Conservative.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/upscale/conservative`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Upscale Image Conservative](https://platform.stability.ai/docs/api-reference#tag/Upscale/paths/~1v2beta~1stable-image~1upscale~1conservative/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | Source image to upscale. |
| `prompt` | body | `string` | yes | Text prompt describing the desired upscale result. |
