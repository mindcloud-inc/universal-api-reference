# Update Task with Missive

Updates a task in your Missive workspace.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tasks/:id`
- **Base URL:** `https://public.missiveapp.com/v1`
- **Official documentation:** [Update Task](https://missiveapp.com/docs/developers/rest-api/endpoints#update-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Task ID. |
| `title` | body | `string` | no | Task title. Max 1000 characters. |
| `description` | body | `string` | no | Task description. Max 10000 characters. |
| `state` | body | `list` | no | Task state. Accepted values: `closed`, `in_progress`, `todo`. |
| `assignees[]` | body | `array<string>` | no | Array of user ID strings. |
| `team` | body | `string` | no | Team ID string. |
| `due_at` | body | `date` | no | Unix timestamp for task due date. |
