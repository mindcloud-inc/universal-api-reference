# Update Epic with Shortcut

## Endpoint

- **Method:** `PUT`
- **Path:** `/epics/:epicPublicId`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [Update Epic](https://developer.shortcut.com/api/rest/v3#Update-Epic)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `epicPublicId` | path | `number` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `state` | body | `string` | no |
| `milestone_id` | body | `number` | no |
| `requested_by_id` | body | `string` | no |
| `epic_state_id` | body | `number` | no |
| `group_id` | body | `string` | no |
| `external_id` | body | `string` | no |
| `deadline` | body | `string` | no |
| `planned_start_date` | body | `string` | no |
| `archived` | body | `boolean` | no |
| `before_id` | body | `number` | no |
| `after_id` | body | `number` | no |
| `completed_at_override` | body | `string` | no |
| `started_at_override` | body | `string` | no |
