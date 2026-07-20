# List Reimbursements with BILL Spend & Expense

Retrieves reimbursements from BILL Spend & Expense.

## Endpoint

- **Method:** `GET`
- **Path:** `spend/reimbursements`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [List Reimbursements](https://developer.bill.com/reference/listreimbursements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | query | `string` | no | Filter expression documented by BILL for this list endpoint. |
| `max` | query | `number` | no | Maximum number of results to return. |
| `nextPage` | query | `string` | no | Next page token returned by the previous list response. |
| `prevPage` | query | `string` | no | Previous page token returned by the previous list response. |
| `sort` | query | `string` | no | Sort expression documented by BILL for this list endpoint. |
