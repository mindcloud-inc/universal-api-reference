# Remove Background From Base64 (v2) with BackgroundCut

Removes an image background in BackgroundCut from a base64 image.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.backgroundcut.co/v2/cut/`
- **Base URL:** `https://backgroundcut.co/api/v1/`
- **Official documentation:** [Remove Background From Base64 (v2)](https://backgroundcut.co/api/docs/v2/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_file_b64` | body | `string` | yes | Base64-encoded source image. |
| `max_resolution` | body | `number` | no | Maximum output resolution in pixels, up to 12000000. |
| `return_type` | body | `list` | no | Output image format. Accepted values: `0`, `1`, `2`, `3`. |
| `quality` | body | `list` | no | Processing quality. Accepted values: `0`, `1`, `2`. |
