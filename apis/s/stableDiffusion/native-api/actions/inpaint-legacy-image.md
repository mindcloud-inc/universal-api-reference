# Inpaint Legacy Image with Stable Diffusion

Inpaints an image with the legacy Stable Diffusion endpoint.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2alpha/generation/stable-image/inpaint`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Inpaint Legacy Image](https://platform.stability.ai/docs/api-reference#tag/v2alpha%2Fgeneration/paths/~1v2alpha~1generation~1stable-image~1inpaint/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | Source image to inpaint. |
| `mode` | body | `string` | yes | Inpainting mode. Use search for prompt-guided region selection. |
| `prompt` | body | `string` | yes | Text prompt describing the desired inpainted output. |
| `search_prompt` | body | `string` | yes | Short description of the region or object to replace when using search mode. |
