# Upload Contact Image with Trust

Uploads a testimonial image to Trust.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/upload-image/:workspaceId`
- **Base URL:** `https://api.usetrust.app/v1`
- **Official documentation:** [Upload Contact Image](https://api-docs.usetrust.io/api-reference-swagger)

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
