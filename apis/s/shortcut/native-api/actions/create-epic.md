# Create Epic with Shortcut

## Endpoint

- **Method:** `POST`
- **Path:** `/epics`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [Create Epic](https://developer.shortcut.com/api/rest/v3#Create-Epic)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |
| `state` | body | `string` | no |
| `milestone_id` | body | `number` | no |
| `requested_by_id` | body | `string` | no |
| `epic_state_id` | body | `number` | no |
| `group_id` | body | `string` | no |
| `external_id` | body | `string` | no |
| `deadline` | body | `string` | no |
| `planned_start_date` | body | `string` | no |
| `completed_at_override` | body | `string` | no |
| `started_at_override` | body | `string` | no |
| `converted_from_story_id` | body | `number` | no |
