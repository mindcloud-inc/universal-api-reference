# Inpaint Image with Stable Diffusion

Inpaints an image in Stable Diffusion.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/inpaint`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Inpaint Image](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1inpaint/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | Source image to edit. |
| `prompt` | body | `string` | yes | Text prompt describing the desired inpainted output. |
