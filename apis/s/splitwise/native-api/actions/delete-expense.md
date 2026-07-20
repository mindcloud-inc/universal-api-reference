# Delete Expense with Splitwise

Deletes an existing expense from Splitwise.

## Endpoint

- **Method:** `POST`
- **Path:** `/delete_expense/[:id]`
- **Base URL:** `https://secure.splitwise.com/api/v3.0`
- **Official documentation:** [Delete Expense](https://dev.splitwise.com/#tag/expenses/paths/~1delete_expense~1{id}/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Splitwise expense ID to delete. |
