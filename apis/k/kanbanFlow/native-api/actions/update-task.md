# Update task with KanbanFlow

Updates an existing task in KanbanFlow.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:taskId`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Update task](https://kanbanflow.com/api-docs/update-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The KanbanFlow task ID. |
| `name` | body | `string` | no | The updated task name. |
| `columnId` | body | `string` | no | The KanbanFlow column ID to move the task into. |
| `description` | body | `string` | no | The updated task description. |
| `color` | body | `string` | no | The lowercase KanbanFlow color value for the task. |
