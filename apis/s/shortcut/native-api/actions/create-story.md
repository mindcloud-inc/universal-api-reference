# Create Story with Shortcut

## Endpoint

- **Method:** `POST`
- **Path:** `/stories`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [Create Story](https://developer.shortcut.com/api/rest/v3#Create-Story)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |
| `story_type` | body | `string` | no |
| `epic_id` | body | `number` | no |
| `requested_by_id` | body | `string` | no |
| `iteration_id` | body | `number` | no |
| `group_id` | body | `string` | no |
| `workflow_state_id` | body | `number` | no |
| `parent_story_id` | body | `number` | no |
| `estimate` | body | `number` | no |
| `project_id` | body | `number` | no |
| `deadline` | body | `string` | no |
| `archived` | body | `boolean` | no |
| `completed_at_override` | body | `string` | no |
| `started_at_override` | body | `string` | no |
| `external_id` | body | `string` | no |
| `source_task_id` | body | `number` | no |
| `story_template_id` | body | `string` | no |
