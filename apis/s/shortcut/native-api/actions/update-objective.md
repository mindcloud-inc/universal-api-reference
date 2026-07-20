# Update Objective with Shortcut

## Endpoint

- **Method:** `PUT`
- **Path:** `/objectives/:objectivePublicId`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [Update Objective](https://developer.shortcut.com/api/rest/v3#Update-Objective)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `objectivePublicId` | path | `number` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `state` | body | `string` | no |
| `started_at_override` | body | `string` | no |
| `completed_at_override` | body | `string` | no |
| `archived` | body | `boolean` | no |
| `before_id` | body | `number` | no |
| `after_id` | body | `number` | no |
