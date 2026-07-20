# Create Expense with Splitwise

Creates a new expense in Splitwise.

## Endpoint

- **Method:** `POST`
- **Path:** `/create_expense`
- **Base URL:** `https://secure.splitwise.com/api/v3.0`
- **Official documentation:** [Create Expense](https://dev.splitwise.com/#tag/expenses/paths/~1create_expense/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | body | `number` | no | Splitwise category ID for the expense. |
| `cost` | body | `string` | yes | Decimal amount as a string with up to 2 decimal places. |
| `currency_code` | body | `string` | no | Splitwise currency code for the expense. |
| `date` | body | `date` | no | When the expense took place. |
| `description` | body | `string` | yes | Short description of the expense. |
| `details` | body | `string` | no | Additional notes for the expense. |
| `group_id` | body | `number` | yes | Splitwise group ID to assign the expense to. |
| `repeat_interval` | body | `string` | no | Expense recurrence interval. |
| `split_equally` | body | `boolean` | yes | When true, Splitwise will create an equal split within the group. |
