# Update Task Hourly Rate with Clockify

Updates a task hourly rate in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/projects/:projectId/tasks/:id/hourly-rate`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Task Hourly Rate](https://docs.developer.clockify.me/#tag/Task/operation/setTaskHourlyRate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string<string>` | yes |
| `id` | path | `string<string>` | yes |
| `amount` | body | `number` | yes |
| `since` | body | `string` | no |
