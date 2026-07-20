# Update Task with Harvest

Updates an existing task in Harvest.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/tasks/:id`
- **Base URL:** `https://api.harvestapp.com`
- **Official documentation:** [Update Task](https://help.getharvest.com/api-v2/tasks-api/tasks/tasks/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `name` | body | `string` | no |
| `billable_by_default` | body | `boolean` | no |
| `default_hourly_rate` | body | `number` | no |
| `is_default` | body | `boolean` | no |
| `is_active` | body | `boolean` | no |
