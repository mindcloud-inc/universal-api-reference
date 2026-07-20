# Create label with KanbanFlow

Creates a new label on a KanbanFlow task.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId/labels`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Create label](https://kanbanflow.com/api-docs/create-label)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
| `name` | body | `string` | yes | The label name. Maximum length: 20. |
| `pinned` | body | `boolean` | no | Whether the label should be pinned. |
