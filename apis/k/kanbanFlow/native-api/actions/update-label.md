# Update label with KanbanFlow

Updates an existing label on a KanbanFlow task.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/labels/by-name/:labelName`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Update label](https://kanbanflow.com/api-docs/update-label)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
| `labelName` | path | `string` | yes | The current label name. Maximum length: 20. |
| `name` | body | `string` | no | The updated label name. Maximum length: 20. |
| `pinned` | body | `boolean` | no | Whether the label should be pinned. |
