# Update Project with Clockodo

Updates a project in your Clockodo account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:id`
- **Base URL:** `https://my.clockodo.com/api/v2`
- **Official documentation:** [Update Project](https://www.clockodo.com/en/api/projects/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `active` | body | `boolean` | no |
| `billable_default` | body | `boolean` | no |
| `billed_completely` | body | `boolean` | no |
| `billed_money` | body | `number` | no |
| `budget_is_hours` | body | `boolean` | no |
| `budget_is_not_strict` | body | `boolean` | no |
| `budget_money` | body | `number` | no |
| `completed` | body | `boolean` | no |
| `customers_id` | body | `string` | no |
| `deadline` | body | `string` | no |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `note` | body | `string` | no |
| `number` | body | `string` | no |
