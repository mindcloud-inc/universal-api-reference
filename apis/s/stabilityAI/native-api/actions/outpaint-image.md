# Outpaint Image with Stability AI

Updates an image in Stability AI with outpainting.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/outpaint`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Outpaint Image](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1outpaint/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Source image file to outpaint. |
