# Create Project with Teamdeck

Creates a new project in Teamdeck.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.teamdeck.io/v1`
- **Official documentation:** [Create Project](https://teamdeck.io/developers/api#operation/addProject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `color` | body | `string` | no |
| `archived` | body | `boolean` | no |
| `enable_time_entry_approval` | body | `boolean` | no |
| `default_approver_id` | body | `number` | no |
| `organization_unit_id` | body | `number` | no |
