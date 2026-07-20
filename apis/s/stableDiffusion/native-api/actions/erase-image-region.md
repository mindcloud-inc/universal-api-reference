# Erase Image Region with Stable Diffusion

Erases a region from an image in Stable Diffusion.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/erase`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Erase Image Region](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1erase/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | Source image to edit. |
| `prompt` | body | `string` | yes | Text prompt describing the region to erase. |
