# Delete subtask with KanbanFlow

Deletes an existing subtask from KanbanFlow.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/:taskId/subtasks/by-index/:index`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Delete subtask](https://kanbanflow.com/api-docs/delete-subtask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
| `index` | path | `number` | yes | The zero-based subtask index. |
