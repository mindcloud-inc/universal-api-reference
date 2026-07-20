# Create Column Task with Queue

Creates a new task for a Queue column.

## Endpoint

- **Method:** `POST`
- **Path:** `columns/:column_id/tasks`
- **Base URL:** `https://app.usequeue.com/api/v1`
- **Official documentation:** [Create Column Task](https://docs.usequeue.com/api-reference/tasks/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `column_id` | path | `string` | yes | Required path parameter from columns/:column_id/tasks. |
| `title` | query | `string` | no | Title of the task |
| `description` | query | `string` | no | Description of the task |
| `priority` | query | `string` | no | Priority level of the task |
| `deadline` | query | `date` | no | Deadline timestamp (ISO 8601) |
| `position` | query | `number` | no | Position of the task in its column |
| `cover_url` | query | `string` | no | Optional cover image URL |
