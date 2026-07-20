# Update Time Entry with Harpoon

Updates an existing time entry in Harpoon.

## Endpoint

- **Method:** `PUT`
- **Path:** `/time_entries/:id`
- **Base URL:** `https://app.harpoonapp.com/api`
- **Official documentation:** [Update Time Entry](https://app.harpoonapp.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `project_id` | body | `number` | no |
| `task_id` | body | `number` | no |
| `date` | body | `date` | no |
| `hours` | body | `number` | no |
| `description` | body | `string` | no |
| `billed_status` | body | `string` | no |
