# Create Task with Hubflo

Creates a new task in Hubflo.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [Create Task](https://hubflo.readme.io/reference/post_api-v2-tasks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |
| `start_time` | body | `string` | no |
| `completed` | body | `boolean` | no |
| `clickup_id` | body | `string` | no |
| `monday_id` | body | `string` | no |
| `kind` | body | `string` | no |
| `visible_by_contact` | body | `boolean` | no |
| `parent_task_id` | body | `string` | no |
| `project_id` | body | `string` | no |
| `project_section_id` | body | `string` | no |
| `contact_id` | body | `string` | no |
| `workspace_id` | body | `string` | no |
| `user_ids` | body | `list<string>` | no |
| `contact_ids` | body | `list<string>` | no |
| `tags` | body | `list<string>` | no |
