# Delete Project with Clockify

Deletes an existing project from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/projects/:projectId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Project](https://docs.developer.clockify.me/#tag/Project/operation/deleteProject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string<string>` | yes |
