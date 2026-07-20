# Create Time Entry with Harvest

Creates a new time entry in Harvest.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/time_entries`
- **Base URL:** `https://api.harvestapp.com`
- **Official documentation:** [Create Time Entry](https://help.getharvest.com/api-v2/timesheets-api/timesheets/time-entries/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_id` | body | `number` | no |
| `project_id` | body | `number` | yes |
| `task_id` | body | `number` | yes |
| `spent_date` | body | `string` | yes |
| `hours` | body | `number` | no |
| `started_time` | body | `string` | no |
| `ended_time` | body | `string` | no |
| `notes` | body | `string` | no |
| `external_reference` | body | `object` | no |
