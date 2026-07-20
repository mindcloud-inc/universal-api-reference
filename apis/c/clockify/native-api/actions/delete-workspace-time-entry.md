# Delete Workspace Time Entry with Clockify

Deletes a workspace time entry from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/time-entries/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Workspace Time Entry](https://docs.developer.clockify.me/#tag/Time-entry/operation/deleteTimeEntry)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `id` | path | `string<string>` | yes |
