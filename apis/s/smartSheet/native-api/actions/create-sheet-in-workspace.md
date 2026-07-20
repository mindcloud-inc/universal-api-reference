# Create Sheet in Workspace with Smartsheet

Creates a new sheet in a Smartsheet workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/sheets`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Create Sheet in Workspace](https://developers.smartsheet.com/api/smartsheet/openapi/sheets/create-sheet-in-workspace)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `number` | yes |
| `name` | body | `string` | yes |
| `columns[]` | body | `array<object>` | no |
| `fromId` | body | `number` | no |
| `include` | query | `string` | no |
