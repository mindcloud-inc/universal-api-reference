# Update Time Entry with Harvest

Updates an existing time entry in Harvest.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/time_entries/:id`
- **Base URL:** `https://api.harvestapp.com`
- **Official documentation:** [Update Time Entry](https://help.getharvest.com/api-v2/timesheets-api/timesheets/time-entries/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `project_id` | body | `number` | no |
| `task_id` | body | `number` | no |
| `spent_date` | body | `string` | no |
| `started_time` | body | `string` | no |
| `ended_time` | body | `string` | no |
| `hours` | body | `number` | no |
| `notes` | body | `string` | no |
| `external_reference` | body | `object` | no |
