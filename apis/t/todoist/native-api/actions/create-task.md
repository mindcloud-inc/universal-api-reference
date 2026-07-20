# Create Task with Todoist

Creates a new task in Todoist.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tasks`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [Create Task](https://developer.todoist.com/api/v1/#tag/Tasks/operation/create_task_api_v1_tasks_post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `content` | body | `string` | yes |
| `description` | body | `string` | no |
| `project_id` | body | `string` | no |
| `section_id` | body | `string` | no |
| `parent_id` | body | `string` | no |
| `order` | body | `number` | no |
| `labels` | body | `list<string>` | no |
| `priority` | body | `number` | no |
| `assignee_id` | body | `number` | no |
| `due_string` | body | `string` | no |
| `due_date` | body | `date` | no |
| `due_datetime` | body | `date` | no |
| `due_lang` | body | `string` | no |
| `duration` | body | `number` | no |
| `duration_unit` | body | `string` | no |
| `deadline_date` | body | `date` | no |
