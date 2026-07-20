# Get tasks by column with KanbanFlow

Retrieves tasks from a KanbanFlow column.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Get tasks by column](https://kanbanflow.com/api-docs/get-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columnId` | query | `string` | yes | The KanbanFlow column ID to list tasks from. |
