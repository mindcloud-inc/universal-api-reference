# Update Story with Shortcut

## Endpoint

- **Method:** `PUT`
- **Path:** `/stories/:storyPublicId`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [Update Story](https://developer.shortcut.com/api/rest/v3#Update-Story)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `storyPublicId` | path | `number` | yes |
| `name` | body | `string` | no |
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
| `before_id` | body | `number` | no |
| `after_id` | body | `number` | no |
| `completed_at_override` | body | `string` | no |
| `started_at_override` | body | `string` | no |
