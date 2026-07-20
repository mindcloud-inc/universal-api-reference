# Delete task with KanbanFlow

Deletes an existing task from KanbanFlow.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Delete task](https://kanbanflow.com/api-docs/delete-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
