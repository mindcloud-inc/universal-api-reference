# Update Task with Hubflo

Updates an existing task in Hubflo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tasks/:id`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [Update Task](https://hubflo.readme.io/reference/patch_api-v2-tasks-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |
| `start_time` | body | `string` | no |
| `completed` | body | `boolean` | no |
| `clickup_id` | body | `string` | no |
| `monday_id` | body | `string` | no |
| `kind` | body | `string` | no |
| `visible_by_contact` | body | `boolean` | no |
| `project_id` | body | `string` | no |
| `project_section_id` | body | `string` | no |
| `contact_id` | body | `string` | no |
| `workspace_id` | body | `string` | no |
| `user_ids` | body | `list<string>` | no |
| `contact_ids` | body | `list<string>` | no |
| `tags` | body | `list<string>` | no |
