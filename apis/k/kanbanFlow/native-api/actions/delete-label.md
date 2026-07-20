# Delete label with KanbanFlow

Deletes an existing label from a KanbanFlow task.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tasks/:taskId/labels/by-name/:labelName`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Delete label](https://kanbanflow.com/api-docs/delete-label)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
| `labelName` | path | `string` | yes | The label name to delete. Maximum length: 20. |
