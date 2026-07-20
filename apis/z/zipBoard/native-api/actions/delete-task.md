# Delete Task with zipBoard

Deletes an existing task from zipBoard.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/issues/tasks/:id`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Delete Task](https://help.zipboard.co/article/181-api-for-issues-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Task record ID to delete. |
