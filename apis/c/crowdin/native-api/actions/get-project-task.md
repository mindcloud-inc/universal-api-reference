# Get Project Task with Crowdin

Retrieves a project task from Crowdin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/tasks/:taskId`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Get Project Task](https://support.crowdin.com/developer/api/v2/#operation/api.projects.tasks.get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `taskId` | path | `number` | yes |
