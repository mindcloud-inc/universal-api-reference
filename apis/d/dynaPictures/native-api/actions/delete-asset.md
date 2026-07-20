# Delete Asset with DynaPictures

Deletes an asset from a DynaPictures workspace.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/media/:workspaceId/assets/:id`
- **Base URL:** `https://api.dynapictures.com`
- **Official documentation:** [Delete Asset](https://dynapictures.com/docs/#delete-asset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ID` | path | `string` | yes | ID of the asset to delete. |
| `workspaceId` | path | `string` | yes | ID of the workspace that owns the asset. |
