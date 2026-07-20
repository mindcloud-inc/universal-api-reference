# Create Expense with FreshBooks

Creates a new expense in FreshBooks for an account.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounting/account/:accountId/expenses/expenses`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Create Expense](https://www.freshbooks.com/api/expenses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
| `expense.amount.amount` | body | `string` | yes | Expense amount value. |
| `expense.amount.code` | body | `string` | yes | ISO currency code. |
| `expense.categoryid` | body | `number` | yes | FreshBooks expense category ID. |
| `expense.date` | body | `string` | yes | Expense date in YYYY-MM-DD format. |
| `expense.staffid` | body | `number` | yes | FreshBooks staff ID. |
| `expense.notes` | body | `string` | no | Expense memo text. |
