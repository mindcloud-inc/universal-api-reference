# Move Task with Todoist

Moves an existing task in Todoist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tasks/:task_id/move`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [Move Task](https://developer.todoist.com/api/v1/#tag/Tasks/operation/move_task_api_v1_tasks__task_id__move_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | ID of the task to move |
| `project_id` | body | `string` | no | Destination project ID |
| `section_id` | body | `string` | no | Destination section ID |
| `parent_id` | body | `string` | no | Destination parent task ID |
