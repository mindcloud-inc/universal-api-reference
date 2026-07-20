# Upload Small Video with Trust

Uploads a small testimonial video to Trust.

## Endpoint

- **Method:** `POST`
- **Path:** `/media/upload-small-video/:workspaceId`
- **Base URL:** `https://api.usetrust.app/v1`
- **Official documentation:** [Upload Small Video](https://api-docs.usetrust.io/api-reference-swagger)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | The video file to upload as multipart form data. |
| `workspaceId` | path | `string` | yes | The Trust workspace ID. |
