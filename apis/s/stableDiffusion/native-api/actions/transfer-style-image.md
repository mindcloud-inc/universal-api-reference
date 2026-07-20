# Transfer Style Image with Stable Diffusion

Transfers image style in Stable Diffusion.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/control/style-transfer`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Transfer Style Image](https://platform.stability.ai/docs/api-reference#tag/Control/paths/~1v2beta~1stable-image~1control~1style-transfer/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `init_image` | body | `string` | yes | Base image to transform. |
| `style_image` | body | `string` | yes | Reference image that provides the style. |
