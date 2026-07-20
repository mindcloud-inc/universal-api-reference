# List Transactions with BILL Spend & Expense

Retrieves transactions from BILL Spend & Expense.

## Endpoint

- **Method:** `GET`
- **Path:** `spend/transactions`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [List Transactions](https://developer.bill.com/reference/listtransactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | query | `string` | no | Filter expression documented by BILL for this list endpoint. |
| `includeReceipts` | query | `boolean` | no | Set true to include transaction receipts in the response. |
| `max` | query | `number` | no | Maximum number of results to return. |
| `nextPage` | query | `string` | no | Next page token returned by the previous list response. |
| `prevPage` | query | `string` | no | Previous page token returned by the previous list response. |
| `showCustomFieldIds` | query | `string` | no | Comma-separated list of custom field IDs or UUIDs to include in the response. |
| `sort` | query | `string` | no | Sort expression documented by BILL for this list endpoint. |
