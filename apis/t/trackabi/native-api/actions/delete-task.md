# Delete Task with Trackabi

Deletes an existing task from Trackabi.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/tasks/:taskId`
- **Base URL:** `https://api.trackabi.com`
- **Official documentation:** [Delete Task](https://trackabi.com/help/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `number` | yes | The unique ID of the task. |
| `recursive` | query | `string` | no | Delete task with subtasks recursively. |
