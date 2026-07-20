# Legacy Upscale Image with Dreamstudio

Creates a legacy upscale job in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2alpha/generation/stable-image/upscale`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Legacy Upscale Image](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Source image file to upscale. |
| `prompt` | body | `string` | yes | Prompt used to guide the upscale. |
