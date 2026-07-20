# Update Expense with Harvest

Updates an existing expense in Harvest.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/expenses/:id`
- **Base URL:** `https://api.harvestapp.com`
- **Official documentation:** [Update Expense](https://help.getharvest.com/api-v2/expenses-api/expenses/expenses/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `project_id` | body | `number` | no |
| `expense_category_id` | body | `number` | no |
| `spent_date` | body | `string` | no |
| `units` | body | `number` | no |
| `total_cost` | body | `number` | no |
| `notes` | body | `string` | no |
| `billable` | body | `boolean` | no |
