# Update comment with KanbanFlow

Updates an existing comment on a KanbanFlow task.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/comments/:commentId`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Update comment](https://kanbanflow.com/api-docs/update-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
| `commentId` | path | `string` | yes | The KanbanFlow comment ID. |
| `text` | body | `string` | no | The updated comment text. |
