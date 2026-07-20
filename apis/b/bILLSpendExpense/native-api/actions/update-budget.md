# Update Budget with BILL Spend & Expense

Updates an existing budget in BILL Spend & Expense.

## Endpoint

- **Method:** `PATCH`
- **Path:** `spend/budgets/:budgetId`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [Update Budget](https://developer.bill.com/reference/updatebudget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `budgetId` | path | `list` | yes | BILL-generated ID or UUID of the budget. |
| `description` | body | `string` | no | Budget description. |
| `limit` | body | `string` | no | Budget spend limit for the current period. |
| `name` | body | `string` | no | Budget name. |
