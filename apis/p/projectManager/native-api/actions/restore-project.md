# Restore Project with ProjectManager

Restores a deleted project in ProjectManager.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/data/projects/:projectId/restore`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Restore Project](https://developer.projectmanager.com/api-reference/project/restore-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the Project to delete |
