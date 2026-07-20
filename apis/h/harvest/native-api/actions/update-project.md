# Update Project with Harvest

Updates an existing project in Harvest.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/projects/:id`
- **Base URL:** `https://api.harvestapp.com`
- **Official documentation:** [Update Project](https://help.getharvest.com/api-v2/projects-api/projects/projects/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `client_id` | body | `number` | no |
| `id` | path | `number` | yes |
| `name` | body | `string` | no |
| `code` | body | `string` | no |
| `is_active` | body | `boolean` | no |
| `is_billable` | body | `boolean` | no |
| `is_fixed_fee` | body | `boolean` | no |
| `bill_by` | body | `string` | no |
| `hourly_rate` | body | `number` | no |
| `budget_by` | body | `string` | no |
| `budget` | body | `number` | no |
| `notes` | body | `string` | no |
| `budget_is_monthly` | body | `boolean` | no |
| `cost_budget` | body | `number` | no |
| `cost_budget_include_expenses` | body | `boolean` | no |
| `notify_when_over_budget` | body | `boolean` | no |
| `over_budget_notification_percentage` | body | `number` | no |
| `show_budget_to_all` | body | `boolean` | no |
| `fee` | body | `number` | no |
| `starts_on` | body | `string` | no |
| `ends_on` | body | `string` | no |
