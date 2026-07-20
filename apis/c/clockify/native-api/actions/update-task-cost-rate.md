# Update Task Cost Rate with Clockify

Updates a task cost rate in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/projects/:projectId/tasks/:id/cost-rate`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Task Cost Rate](https://docs.developer.clockify.me/#tag/Task/operation/setTaskCostRate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string<string>` | yes |
| `id` | path | `string<string>` | yes |
| `amount` | body | `number` | yes |
| `since` | body | `string` | no |
