# List Users with BILL Spend & Expense

Retrieves users from BILL Spend & Expense.

## Endpoint

- **Method:** `GET`
- **Path:** `spend/users`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [List Users](https://developer.bill.com/reference/listusers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | query | `string` | no | Filter expression documented by BILL for this list endpoint. |
| `max` | query | `string` | no | Maximum number of results to return. |
| `nextPage` | query | `string` | no | Next page token returned by the previous list response. |
| `prevPage` | query | `string` | no | Previous page token returned by the previous list response. |
