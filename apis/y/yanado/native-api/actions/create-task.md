# Create Task with Yanado

Creates a new task in Yanado.

## Endpoint

- **Method:** `POST`
- **Path:** `/public-api/tasks`
- **Base URL:** `https://api.yanado.com`
- **Official documentation:** [Create Task](https://api.yanado.com/docs/#create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | body | `string` | yes | Yanado list ID where the task should be created. |
| `name` | body | `string` | yes | Task name. |
| `statusId` | body | `string` | yes | Yanado status ID for the new task. |
| `assigneeId` | body | `string` | no | Assign the new task to this user ID. |
| `description` | body | `string` | no | Task description. |
| `dueDate` | body | `date` | no | Task due date. |
| `form` | body | `object` | no | Additional task form payload. |
| `threadEmail` | body | `string` | no | Participant email for the thread. |
| `threadId` | body | `string` | no | Thread ID. |
| `threadName` | body | `string` | no | Thread name. |
| `threadSubject` | body | `string` | no | Thread subject. |
