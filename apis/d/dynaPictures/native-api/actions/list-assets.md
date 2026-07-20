# List Assets with DynaPictures

Retrieves assets from a DynaPictures workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/media/:workspaceId/assets`
- **Base URL:** `https://api.dynapictures.com`
- **Official documentation:** [List Assets](https://dynapictures.com/docs/#asset-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | ID of the workspace whose assets to list. |
