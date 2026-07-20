# Add or Update Budget Member with BILL Spend & Expense

Adds or updates a budget member in BILL Spend & Expense.

## Endpoint

- **Method:** `PUT`
- **Path:** `spend/budgets/:budgetId/members/:userId`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [Add or Update Budget Member](https://developer.bill.com/reference/upsertbudgetmember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `budgetId` | path | `list` | yes | BILL-generated ID or UUID of the budget. |
| `limit` | body | `number` | no | Funds assigned to the user in the current budget period. |
| `recurringLimit` | body | `number` | no | Funds assigned to the user in future budget periods. |
| `role` | body | `string` | no | Budget user role. |
| `shareBudgetFunds` | body | `boolean` | no | Set true to share all budget funds with the user. |
| `userId` | path | `list` | yes | BILL-generated ID or UUID of the user. |
