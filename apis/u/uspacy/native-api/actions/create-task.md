# Create Task with Uspacy

Creates a new task in Uspacy.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/v1/tasks`
- **Base URL:** `https://{site}`
- **Official documentation:** [Create Task](https://uspacy.readme.io/reference/post_tasks-v1-tasks-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The task title. |
| `created_by` | body | `number` | yes | The user ID that created the task. |
| `setter_id` | body | `string` | yes | The user ID who assigned the task. |
