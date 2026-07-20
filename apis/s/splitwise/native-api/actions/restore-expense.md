# Restore Expense with Splitwise

Restores a deleted expense in Splitwise.

## Endpoint

- **Method:** `POST`
- **Path:** `/undelete_expense/[:id]`
- **Base URL:** `https://secure.splitwise.com/api/v3.0`
- **Official documentation:** [Restore Expense](https://dev.splitwise.com/#tag/expenses/paths/~1undelete_expense~1{id}/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Splitwise expense ID to restore. |
