# Get Asset with DynaPictures

Retrieves an asset from a DynaPictures workspace by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/media/:workspaceId/assets/:id`
- **Base URL:** `https://api.dynapictures.com`
- **Official documentation:** [Get Asset](https://dynapictures.com/docs/#load-asset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ID` | path | `string` | yes | ID of the asset to load. |
| `workspaceId` | path | `string` | yes | ID of the workspace that owns the asset. |
