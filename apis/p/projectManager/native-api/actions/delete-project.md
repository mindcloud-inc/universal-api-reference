# Delete Project with ProjectManager

Deletes an existing project from ProjectManager.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/data/projects/:projectId`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Delete Project](https://developer.projectmanager.com/api-reference/project/delete-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the Project to delete |
| `hardDelete` | query | `boolean` | no | Hard delete project true or false |
