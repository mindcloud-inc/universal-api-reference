# Get Workspace Time Entry with Clockify

Retrieves a workspace time entry from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/time-entries/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Workspace Time Entry](https://docs.developer.clockify.me/#tag/Time-entry/operation/getTimeEntry)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `id` | path | `string<string>` | yes |
| `hydrated` | query | `boolean` | no |
