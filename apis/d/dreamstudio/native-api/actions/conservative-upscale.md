# Conservative Upscale with Dreamstudio

Creates a conservative 4K upscale in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/upscale/conservative`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Conservative Upscale](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Source image file to upscale conservatively. |
| `prompt` | body | `string` | yes | Prompt used to guide the upscale. |
