# Upload GIF with Giphy

Uploads a GIF to Giphy.

## Endpoint

- **Method:** `POST`
- **Path:** `https://upload.giphy.com/v1/gifs`
- **Base URL:** `https://api.giphy.com/`
- **Official documentation:** [Upload GIF](https://developers.giphy.com/docs/api/endpoint/#upload)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `source_image_url` | body | `string` | no |
| `file` | body | `file` | no |
| `tags` | body | `string` | no |
| `source_post_url` | body | `string` | no |
