# Create Task with Clientary

Creates a new task in Clientary.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [Create Task](https://www.clientary.com/api/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task.assignee_id` | body | `number` | no | Optionally assign the task to a staff member. |
| `task.project_id` | body | `number` | no | Optionally assign the task to a project. |
| `task.title` | body | `string` | yes | The task title. |
