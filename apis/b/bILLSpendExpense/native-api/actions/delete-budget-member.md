# Delete Budget Member with BILL Spend & Expense

Deletes an existing budget member from BILL Spend & Expense.

## Endpoint

- **Method:** `DELETE`
- **Path:** `spend/budgets/:budgetId/members/:userId`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [Delete Budget Member](https://developer.bill.com/reference/deletebudgetmember)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `budgetId` | path | `list` | yes | BILL-generated ID or UUID of the budget. |
| `userId` | path | `list` | yes | BILL-generated ID or UUID of the user. |
