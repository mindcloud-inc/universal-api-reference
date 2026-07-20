# Transfer Image Style with Stability AI

Updates an image in Stability AI with style transfer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/control/style-transfer`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Transfer Image Style](https://platform.stability.ai/docs/api-reference#tag/Control/paths/~1v2beta~1stable-image~1control~1style-transfer/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `init_image` | body | `file` | yes | Target image file whose composition/content should receive the style. |
| `style_image` | body | `file` | yes | Reference image file providing the style. |
