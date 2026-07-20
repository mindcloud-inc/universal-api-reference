# Create Folder in Workspace with Smartsheet

Creates a new folder in a Smartsheet workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/folders`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Create Folder in Workspace](https://developers.smartsheet.com/api/smartsheet/openapi/folders/create-folder-in-workspace)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `number` | yes |
| `name` | body | `string` | yes |
