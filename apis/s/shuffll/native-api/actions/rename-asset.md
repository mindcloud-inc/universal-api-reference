# Rename Asset with Shuffll

Updates an asset name in Shuffll.

## Endpoint

- **Method:** `PUT`
- **Path:** `/auth/organization/:organizationId/workspace/:workspaceId/assets/:assetId/file`
- **Base URL:** `https://api.shuffll.com/api/v1`
- **Official documentation:** [Rename Asset](https://api-docs.shuffll.com/apis/assets/renameasset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assetId` | path | `string` | yes | Shuffll asset id. |
| `newName` | body | `string` | yes | New asset display name. |
| `organizationId` | path | `string` | yes | Shuffll organization id. |
| `workspaceId` | path | `string` | yes | Shuffll workspace id. |
