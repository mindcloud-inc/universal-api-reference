# Upload Image with Ghost

Uploads an image to Ghost.

## Endpoint

- **Method:** `POST`
- **Path:** `/images/upload/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Upload Image](https://docs.ghost.org/admin-api/images/uploading-an-image)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Image file contents to upload. |
| `purpose` | body | `string` | no | Upload purpose for the image. |
| `ref` | body | `string` | no | Reference string returned with the uploaded image. |
