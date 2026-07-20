# Upload Asset with DynaPictures

Uploads an asset to a DynaPictures workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/media/:workspaceId/assets`
- **Base URL:** `https://api.dynapictures.com`
- **Official documentation:** [Upload Asset](https://dynapictures.com/docs/#upload-an-image)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Image file to upload. |
| `workspaceId` | path | `string` | yes | ID of the workspace to upload the asset into. |
