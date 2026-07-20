# Update Task with Todoist

Updates an existing task in Todoist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tasks/:task_id`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [Update Task](https://developer.todoist.com/api/v1/#tag/Tasks/operation/update_task_api_v1_tasks__task_id__post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task_id` | path | `string` | yes |
| `content` | body | `string` | no |
| `description` | body | `string` | no |
| `labels` | body | `list<string>` | no |
| `priority` | body | `number` | no |
| `due_string` | body | `string` | no |
| `due_date` | body | `date` | no |
| `due_datetime` | body | `date` | no |
| `due_lang` | body | `string` | no |
| `duration` | body | `number` | no |
| `duration_unit` | body | `string` | no |
| `deadline_date` | body | `date` | no |
