# List Expense Comments with Splitwise

Retrieves comments for an expense in Splitwise.

## Endpoint

- **Method:** `GET`
- **Path:** `/get_comments`
- **Base URL:** `https://secure.splitwise.com/api/v3.0`
- **Official documentation:** [List Expense Comments](https://dev.splitwise.com/#tag/comments/paths/~1get_comments/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expense_id` | query | `number` | yes | Splitwise expense ID whose comments should be returned. |
