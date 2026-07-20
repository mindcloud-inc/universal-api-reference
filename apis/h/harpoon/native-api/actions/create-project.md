# Create Project with Harpoon

Creates a new project in Harpoon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://app.harpoonapp.com/api`
- **Official documentation:** [Create Project](https://app.harpoonapp.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `client_id` | body | `number` | no |
| `project_name` | body | `string` | no |
| `type` | body | `string` | no |
| `project_status` | body | `string` | no |
| `project_start` | body | `date` | no |
| `project_end` | body | `date` | no |
| `budget` | body | `number` | no |
| `budget_reset` | body | `string` | no |
| `track_unbilled_hours_expected_revenue` | body | `boolean` | no |
| `custom_task_rates` | body | `object` | no |
