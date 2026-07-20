# Creative Upscale Image with Stability AI

Upscales an image in Stability AI with creative mode.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/upscale/creative`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Creative Upscale Image](https://platform.stability.ai/docs/api-reference#tag/Upscale/paths/~1v2beta~1stable-image~1upscale~1creative/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Source image file to upscale. |
| `prompt` | body | `string` | yes | Prompt guiding the creative upscale result. |
