# Style Transfer with Dreamstudio

Applies reference image styles to an image in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/control/style-transfer`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Style Transfer](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `init_image` | body | `file` | yes | Base image to stylize. |
| `style_image` | body | `file` | yes | Reference image that provides the target style. |
