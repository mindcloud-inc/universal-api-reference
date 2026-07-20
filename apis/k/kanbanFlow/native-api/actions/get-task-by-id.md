# Get task by ID with KanbanFlow

Retrieves a task from KanbanFlow by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Get task by ID](https://kanbanflow.com/api-docs/get-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
