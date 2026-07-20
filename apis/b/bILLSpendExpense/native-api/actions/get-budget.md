# Get Budget with BILL Spend & Expense

Retrieves a budget from BILL Spend & Expense.

## Endpoint

- **Method:** `GET`
- **Path:** `spend/budgets/:budgetId`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [Get Budget](https://developer.bill.com/reference/getbudget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `budgetId` | path | `list` | yes | BILL-generated ID or UUID of the budget. |
