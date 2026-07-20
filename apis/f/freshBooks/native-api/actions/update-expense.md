# Update Expense with FreshBooks

Updates an existing expense in FreshBooks for an account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounting/account/:accountId/expenses/expenses/:expenseId`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Update Expense](https://www.freshbooks.com/api/expenses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
| `expenseId` | path | `string` | yes | FreshBooks expense ID. |
| `expense.amount.amount` | body | `string` | no | Expense amount value. |
| `expense.amount.code` | body | `string` | no | ISO currency code. |
| `expense.notes` | body | `string` | no | Expense memo text. |
