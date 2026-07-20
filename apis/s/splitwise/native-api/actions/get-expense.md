# Get Expense with Splitwise

Retrieves expense details from Splitwise.

## Endpoint

- **Method:** `GET`
- **Path:** `/get_expense/[:id]`
- **Base URL:** `https://secure.splitwise.com/api/v3.0`
- **Official documentation:** [Get Expense](https://dev.splitwise.com/#tag/expenses/paths/~1get_expense~1{id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Splitwise expense ID to retrieve. |
