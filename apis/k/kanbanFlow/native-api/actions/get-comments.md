# Get comments with KanbanFlow

Retrieves all comments for a KanbanFlow task.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:taskId/comments`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Get comments](https://kanbanflow.com/api-docs/get-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
