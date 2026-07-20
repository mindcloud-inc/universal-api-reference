# Create Expense with WebWork Time Tracker

Creates an expense in WebWork Time Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/expenses`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Create Expense](https://api-docs.webwork-tracker.com/api/expenses/createexpense)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | ID of the workspace. |
| `expense_name` | body | `string` | yes | Name of the expense. Required by the provider runtime validation. |
| `amount` | body | `number` | no | Expense amount. |
| `category_id` | body | `string` | no | Expense category ID. |
| `description` | body | `string` | no | Expense description. |
| `date` | body | `string` | no | Expense date in YYYY-MM-DD format. |
