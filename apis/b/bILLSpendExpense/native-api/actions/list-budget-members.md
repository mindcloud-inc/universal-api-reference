# List Budget Members with BILL Spend & Expense

Retrieves members for a budget in BILL Spend & Expense.

## Endpoint

- **Method:** `GET`
- **Path:** `spend/budgets/:budgetId/members`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [List Budget Members](https://developer.bill.com/reference/listbudgetmembers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `budgetId` | path | `list` | yes | BILL-generated ID or UUID of the budget. |
| `max` | query | `number` | no | Maximum number of results to return. |
| `nextPage` | query | `string` | no | Next page token returned by the previous list response. |
| `prevPage` | query | `string` | no | Previous page token returned by the previous list response. |
