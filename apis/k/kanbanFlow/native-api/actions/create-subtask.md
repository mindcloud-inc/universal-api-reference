# Create subtask with KanbanFlow

Creates a new subtask in KanbanFlow.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/subtasks`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Create subtask](https://kanbanflow.com/api-docs/create-subtask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
| `name` | body | `string` | yes | The subtask name. |
| `finished` | body | `boolean` | no | Whether the subtask is complete. |
