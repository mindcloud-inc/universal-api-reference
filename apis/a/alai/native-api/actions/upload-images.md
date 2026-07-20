# Upload Images with Alai

Uploads images to Alai and returns image IDs.

## Endpoint

- **Method:** `POST`
- **Path:** `/upload-images`
- **Base URL:** `https://slides-api.getalai.com/api/v1`
- **Official documentation:** [Upload Images](https://docs.getalai.com/api/upload-images)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files` | body | `file` | yes | Image files to upload for later presentation generation. |
