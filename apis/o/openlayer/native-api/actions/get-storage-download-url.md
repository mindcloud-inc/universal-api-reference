# Get Storage Download URL with Openlayer

Retrieves a storage download URL from Openlayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/storage/presigned-url`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [Get Storage Download URL](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storageUri` | query | `string` | yes | Stored object URI. |
| `workspaceId` | query | `string` | no | Workspace scope for the storage URL. |
