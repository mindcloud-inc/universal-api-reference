# Submit Async Upscale with Stable Diffusion

Submits an asynchronous upscale request to Stable Diffusion.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2alpha/generation/stable-image/upscale`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Submit Async Upscale](https://platform.stability.ai/docs/api-reference#tag/v2alpha%2Fgeneration/paths/~1v2alpha~1generation~1stable-image~1upscale/post)

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
