# Update Project with Shortcut

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectPublicId`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [Update Project](https://developer.shortcut.com/api/rest/v3#Update-Project)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectPublicId` | path | `number` | yes |
| `name` | body | `string` | no |
| `team_id` | body | `number` | no |
| `description` | body | `string` | no |
| `color` | body | `string` | no |
| `archived` | body | `boolean` | no |
| `abbreviation` | body | `string` | no |
| `days_to_thermometer` | body | `number` | no |
| `show_thermometer` | body | `boolean` | no |
