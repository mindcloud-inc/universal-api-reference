# Remove Background From File (v1) with BackgroundCut

Removes an image background in BackgroundCut from an uploaded file.

## Endpoint

- **Method:** `POST`
- **Path:** `cut/`
- **Base URL:** `https://backgroundcut.co/api/v1/`
- **Official documentation:** [Remove Background From File (v1)](https://backgroundcut.co/api/docs/v1/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Source image file. |
| `max_resolution` | body | `number` | no | Maximum output resolution in pixels, up to 12000000. |
| `return_format` | body | `list` | no | Output format. Accepted values: `0`, `1`. |
| `quality` | body | `list` | no | Processing quality. Accepted values: `0`, `1`, `2`. |
