# Upload File with Dify

Uploads a file to Dify.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/upload`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Upload File](https://docs.dify.ai/api-reference/files/upload-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | File to upload. |
| `user` | body | `string` | no | User identifier. |
