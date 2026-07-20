# Fast Upscale with Dreamstudio

Creates a fast 4x upscale in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/upscale/fast`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Fast Upscale](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Source image file to upscale quickly. |
