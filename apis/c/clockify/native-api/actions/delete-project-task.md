# Delete Project Task with Clockify

Deletes an existing project task from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/projects/:projectId/tasks/:taskId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Project Task](https://docs.developer.clockify.me/#tag/Task/operation/deleteTask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string<string>` | yes |
| `taskId` | path | `string<string>` | yes |
