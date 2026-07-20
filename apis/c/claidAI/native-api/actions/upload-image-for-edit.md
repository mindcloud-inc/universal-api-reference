# Upload Image For Edit with Claid AI

Creates an edited image in Claid AI from upload.

## Endpoint

- **Method:** `POST`
- **Path:** `image/edit/upload`
- **Base URL:** `https://api.claid.ai/v1`
- **Official documentation:** [Upload Image For Edit](https://docs.claid.ai/image-editing-api/upload-api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `string` | yes | JSON string containing the operations and optional output payload for the upload request. |
| `file` | body | `file` | yes | — |
