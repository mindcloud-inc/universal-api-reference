# Create Time Entry with Harpoon

Creates a new time entry in Harpoon.

## Endpoint

- **Method:** `POST`
- **Path:** `/time_entries`
- **Base URL:** `https://app.harpoonapp.com/api`
- **Official documentation:** [Create Time Entry](https://app.harpoonapp.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | body | `number` | no |
| `task_id` | body | `number` | no |
| `date` | body | `date` | no |
| `hours` | body | `number` | yes |
| `description` | body | `string` | no |
| `profile_id` | body | `number` | no |
