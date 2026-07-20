# Get Project Task with Clockify

Retrieves a specific project task from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/projects/:projectId/tasks/:taskId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Project Task](https://docs.developer.clockify.me/#tag/Task/operation/getTask)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string<string>` | yes |
| `taskId` | path | `string<string>` | yes |
