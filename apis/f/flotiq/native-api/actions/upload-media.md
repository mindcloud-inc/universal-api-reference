# Upload Media with Flotiq

Uploads a media file to Flotiq.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.flotiq.com/api/media`
- **Base URL:** `https://api.flotiq.com/api/v1`
- **Official documentation:** [Upload Media](https://flotiq.com/docs/API/media-library/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The media file to upload. |
| `type` | body | `list` | yes | The uploaded media type: image or file. Accepted values: `0`, `1`. |
