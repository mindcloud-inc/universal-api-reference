# Create Project with Harvest

Creates a new project in Harvest.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/projects`
- **Base URL:** `https://api.harvestapp.com`
- **Official documentation:** [Create Project](https://help.getharvest.com/api-v2/projects-api/projects/projects/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `client_id` | body | `number` | yes |
| `name` | body | `string` | yes |
| `code` | body | `string` | no |
| `is_active` | body | `boolean` | no |
| `is_billable` | body | `boolean` | yes |
| `is_fixed_fee` | body | `boolean` | no |
| `bill_by` | body | `string` | yes |
| `hourly_rate` | body | `number` | no |
| `budget_by` | body | `string` | yes |
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
