# Add comment with KanbanFlow

Creates a new comment on a KanbanFlow task.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/comments`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Add comment](https://kanbanflow.com/api-docs/add-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
| `text` | body | `string` | yes | The comment text. |
