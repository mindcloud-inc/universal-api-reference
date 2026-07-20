# Upload Media Image with Trust

Uploads an image for the Trust video editor.

## Endpoint

- **Method:** `POST`
- **Path:** `/media/upload-image/:workspaceId`
- **Base URL:** `https://api.usetrust.app/v1`
- **Official documentation:** [Upload Media Image](https://api-docs.usetrust.io/api-reference-swagger)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | The image file to upload as multipart form data. |
| `workspaceId` | path | `string` | yes | The Trust workspace ID. |
