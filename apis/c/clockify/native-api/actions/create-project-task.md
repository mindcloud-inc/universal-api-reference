# Create Project Task with Clockify

Creates a new project task in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/projects/:projectId/tasks`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Project Task](https://docs.developer.clockify.me/#tag/Task/operation/createTask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string` | yes |
| `contains-assignee` | query | `boolean` | no |
| `name` | body | `string` | yes |
| `assigneeId` | body | `string` | no |
| `assigneeIds[]` | body | `array<string>` | no |
| `budgetEstimate` | body | `number` | no |
| `estimate` | body | `string` | no |
| `id` | body | `string` | no |
| `status` | body | `string` | no |
| `userGroupIds[]` | body | `array<string>` | no |
