# Upload Media with Wbiztool

Uploads a media file to Wbiztool.

## Endpoint

- **Method:** `POST`
- **Path:** `/media/upload/`
- **Base URL:** `https://wbiztool.com/api/v1`
- **Official documentation:** [Upload Media](https://wbiztool.com/docs/media-upload-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `media_file` | body | `file` | yes | Binary media file to upload. |
