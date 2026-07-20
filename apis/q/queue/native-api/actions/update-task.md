# Update Task with Queue

Updates an existing task in Queue.

## Endpoint

- **Method:** `PATCH`
- **Path:** `tasks/:task_id`
- **Base URL:** `https://app.usequeue.com/api/v1`
- **Official documentation:** [Update Task](https://docs.usequeue.com/api-reference/tasks/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | — |
| `title` | query | `string` | no | Title of the task |
| `description` | query | `string` | no | Description of the task |
| `priority` | query | `string` | no | Priority level of the task |
| `deadline` | query | `date` | no | Deadline timestamp (ISO 8601) |
| `position` | query | `number` | no | Position of the task in its column |
| `cover_url` | query | `string` | no | Optional cover image URL |
