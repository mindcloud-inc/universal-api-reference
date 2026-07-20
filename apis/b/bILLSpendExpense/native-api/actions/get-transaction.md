# Get Transaction with BILL Spend & Expense

Retrieves a transaction from BILL Spend & Expense.

## Endpoint

- **Method:** `GET`
- **Path:** `spend/transactions/:transactionId`
- **Base URL:** `https://gateway.{environment}.bill.com/connect/v3`
- **Official documentation:** [Get Transaction](https://developer.bill.com/reference/gettransaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `showCustomFieldIds` | query | `string` | no | Comma-separated list of custom field IDs or UUIDs to include in the response. |
| `transactionId` | path | `list` | yes | BILL-generated ID or UUID of the transaction. |
