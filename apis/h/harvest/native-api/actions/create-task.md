# Create Task with Harvest

Creates a new task in Harvest.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/tasks`
- **Base URL:** `https://api.harvestapp.com`
- **Official documentation:** [Create Task](https://help.getharvest.com/api-v2/tasks-api/tasks/tasks/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `billable_by_default` | body | `boolean` | no |
| `default_hourly_rate` | body | `number` | no |
| `is_default` | body | `boolean` | no |
| `is_active` | body | `boolean` | no |
