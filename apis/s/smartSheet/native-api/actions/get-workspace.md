# Get Workspace with Smartsheet

Retrieves a workspace from Smartsheet.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Get Workspace](https://developers.smartsheet.com/api/smartsheet/openapi/workspaces/get-workspace)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `number` | yes |
| `include` | query | `string` | no |
| `loadAll` | query | `boolean` | no |
