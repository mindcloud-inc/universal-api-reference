# Upload Image with Glam AI

Uploads an image to Glam AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/upload`
- **Base URL:** `https://api.glam.ai/api/v1`
- **Official documentation:** [Upload Image](https://glam-ai.readme.io/reference/upload_image_upload_post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Image file to upload. |
