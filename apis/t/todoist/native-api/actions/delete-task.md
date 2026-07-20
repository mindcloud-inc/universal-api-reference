# Delete Task with Todoist

Deletes an existing task from Todoist.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/tasks/:task_id`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [Delete Task](https://developer.todoist.com/api/v1/#tag/Tasks/operation/delete_task_api_v1_tasks__task_id__delete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task_id` | path | `string` | yes |
