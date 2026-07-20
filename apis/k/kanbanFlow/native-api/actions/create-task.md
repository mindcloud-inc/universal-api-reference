# Create task with KanbanFlow

Creates a new task in KanbanFlow.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Create task](https://kanbanflow.com/api-docs/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The task name. |
| `columnId` | body | `string` | yes | The KanbanFlow column ID where the task will be created. |
| `description` | body | `string` | no | The task description. |
| `color` | body | `string` | no | The lowercase KanbanFlow color value for the task. |
