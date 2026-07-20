# Remove Background with Stable Diffusion

Removes an image background in Stable Diffusion.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/remove-background`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Remove Background](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1remove-background/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | Source image to process. |
