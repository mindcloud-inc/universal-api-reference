# Close Task with Todoist

Closes an existing task in Todoist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tasks/:task_id/close`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [Close Task](https://developer.todoist.com/api/v1/#tag/Tasks/operation/close_task_api_v1_tasks__task_id__close_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | ID of the task to close |
