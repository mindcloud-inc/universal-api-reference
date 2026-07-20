# Create Project with Clockodo

Creates a project in your Clockodo account.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://my.clockodo.com/api/v2`
- **Official documentation:** [Create Project](https://www.clockodo.com/en/api/projects/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `active` | body | `boolean` | no |
| `billable_default` | body | `boolean` | no |
| `budget_is_hours` | body | `boolean` | no |
| `budget_is_not_strict` | body | `boolean` | no |
| `budget_money` | body | `number` | no |
| `customers_id` | body | `string` | yes |
| `deadline` | body | `string` | no |
| `name` | body | `string` | yes |
| `note` | body | `string` | no |
| `number` | body | `string` | no |
