# Delete comment with KanbanFlow

Deletes an existing comment from a KanbanFlow task.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/:taskId/comments/:commentId`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Delete comment](https://kanbanflow.com/api-docs/delete-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
| `commentId` | path | `string` | yes | The KanbanFlow comment ID. |
