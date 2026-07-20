# Create Storage Upload URL with Openlayer

Creates a storage upload URL in Openlayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/storage/presigned-url`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [Create Storage Upload URL](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectName` | query | `string` | yes | Object name to upload. |
| `workspaceId` | query | `string` | no | Workspace scope for the upload URL. |
