# Update Project Task with Clockify

Updates an existing project task in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/projects/:projectId/tasks/:taskId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Project Task](https://docs.developer.clockify.me/#tag/Task/operation/updateTask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string` | yes |
| `taskId` | path | `string` | yes |
| `contains-assignee` | query | `boolean` | no |
| `membership-status` | query | `string` | no |
| `name` | body | `string` | yes |
| `assigneeId` | body | `string` | no |
| `assigneeIds[]` | body | `array<string>` | no |
| `billable` | body | `boolean` | no |
| `budgetEstimate` | body | `number` | no |
| `estimate` | body | `string` | no |
| `status` | body | `string` | no |
| `userGroupIds[]` | body | `array<string>` | no |
