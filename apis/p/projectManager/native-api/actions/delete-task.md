# Delete Task with ProjectManager

Deletes an existing task from ProjectManager.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/data/tasks/:taskId`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Delete Task](https://developer.projectmanager.com/api-reference/task/delete-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Unique identifier of the Task to delete |
