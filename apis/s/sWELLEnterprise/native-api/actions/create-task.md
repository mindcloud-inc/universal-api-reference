# Create Task with SWELLEnterprise

Creates a new task in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/tasks`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Create Task](https://dashboard.swellsystem.com/docs#projects-tasks-POSTapi-v1-projects-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The task title. |
| `project_id` | body | `number` | no | The project ID. |
| `status_id` | body | `number` | yes | The status ID. |
| `description` | body | `string` | no | The task description. |
