# Update Expense with Splitwise

Updates an existing expense in Splitwise.

## Endpoint

- **Method:** `POST`
- **Path:** `/update_expense/[:id]`
- **Base URL:** `https://secure.splitwise.com/api/v3.0`
- **Official documentation:** [Update Expense](https://dev.splitwise.com/#tag/expenses/paths/~1update_expense~1{id}/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | body | `number` | no | Updated Splitwise category ID for the expense. |
| `cost` | body | `string` | no | Updated decimal amount as a string with up to 2 decimal places. |
| `currency_code` | body | `string` | no | Updated Splitwise currency code for the expense. |
| `date` | body | `date` | no | Updated timestamp for when the expense took place. |
| `description` | body | `string` | no | Updated short description of the expense. |
| `details` | body | `string` | no | Updated additional notes for the expense. |
| `group_id` | body | `number` | no | Updated Splitwise group ID for the expense. |
| `id` | path | `number` | yes | Splitwise expense ID to update. |
| `repeat_interval` | body | `string` | no | Updated expense recurrence interval. |
