# Create Expense with Harvest

Creates a new expense in Harvest.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/expenses`
- **Base URL:** `https://api.harvestapp.com`
- **Official documentation:** [Create Expense](https://help.getharvest.com/api-v2/expenses-api/expenses/expenses/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_id` | body | `number` | no |
| `project_id` | body | `number` | yes |
| `expense_category_id` | body | `number` | yes |
| `spent_date` | body | `string` | yes |
| `units` | body | `number` | no |
| `total_cost` | body | `number` | no |
| `notes` | body | `string` | no |
| `billable` | body | `boolean` | no |
