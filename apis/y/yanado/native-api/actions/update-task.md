# Update Task with Yanado

Updates an existing task in Yanado.

## Endpoint

- **Method:** `PUT`
- **Path:** `/public-api/tasks/:taskId`
- **Base URL:** `https://api.yanado.com`
- **Official documentation:** [Update Task](https://api.yanado.com/docs/#update-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Yanado task ID. |
| `archived` | body | `boolean` | no | Archive state for the task. |
| `assigneeId` | body | `string` | no | Assign the task to this user ID. |
| `description` | body | `string` | no | Task description. |
| `dueDate` | body | `date` | no | Task due date. |
| `form` | body | `object` | no | Additional task form payload. |
| `listId` | body | `string` | no | Yanado list ID for the task. |
| `name` | body | `string` | no | Task name. |
| `statusId` | body | `string` | no | Yanado status ID for the task. |
