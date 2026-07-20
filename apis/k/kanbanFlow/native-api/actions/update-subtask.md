# Update subtask with KanbanFlow

Updates an existing subtask in KanbanFlow.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/subtasks/by-index/:index`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Update subtask](https://kanbanflow.com/api-docs/update-subtask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
| `index` | path | `number` | yes | The zero-based subtask index. |
| `name` | body | `string` | no | The updated subtask name. |
| `finished` | body | `boolean` | no | Whether the subtask is complete. |
