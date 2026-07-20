# Update Workspace with OpnForm

Updates an existing workspace in OpnForm.

## Endpoint

- **Method:** `PUT`
- **Path:** `/open/workspaces/:workspaceId`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [Update Workspace](https://docs.opnform.com/api-reference/workspaces/update-workspace)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `number` | yes |
| `name` | body | `string` | yes |
| `emoji` | body | `string` | no |
