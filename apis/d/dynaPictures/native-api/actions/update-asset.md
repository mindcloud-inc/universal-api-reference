# Update Asset with DynaPictures

Updates an asset in a DynaPictures workspace.

## Endpoint

- **Method:** `PUT`
- **Path:** `/media/:workspaceId/assets/:id`
- **Base URL:** `https://api.dynapictures.com`
- **Official documentation:** [Update Asset](https://dynapictures.com/docs/#update-asset)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Replacement image file. |
| `ID` | path | `string` | yes | ID of the asset to replace. |
| `workspaceId` | path | `string` | yes | ID of the workspace that owns the asset. |
