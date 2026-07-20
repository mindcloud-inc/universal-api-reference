# Create Project with Shortcut

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [Create Project](https://developer.shortcut.com/api/rest/v3#Create-Project)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `team_id` | body | `number` | yes |
| `description` | body | `string` | no |
| `color` | body | `string` | no |
| `iteration_length` | body | `number` | no |
| `abbreviation` | body | `string` | no |
| `external_id` | body | `string` | no |
| `start_time` | body | `string` | no |
