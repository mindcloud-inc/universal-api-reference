# Delete Project with Todoist

Deletes an existing project from Todoist.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/projects/:project_id`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [Delete Project](https://developer.todoist.com/api/v1/#tag/Projects/operation/delete_project_api_v1_projects__project_id__delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project identifier. |
