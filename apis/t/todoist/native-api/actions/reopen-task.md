# Reopen Task with Todoist

Reopens an existing task in Todoist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tasks/:task_id/reopen`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [Reopen Task](https://developer.todoist.com/api/v1/#tag/Tasks/operation/reopen_task_api_v1_tasks__task_id__reopen_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | ID of the task to reopen |
