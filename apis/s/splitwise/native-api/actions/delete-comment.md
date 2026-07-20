# Delete Comment with Splitwise

Deletes an expense comment from Splitwise.

## Endpoint

- **Method:** `POST`
- **Path:** `/delete_comment/[:id]`
- **Base URL:** `https://secure.splitwise.com/api/v3.0`
- **Official documentation:** [Delete Comment](https://dev.splitwise.com/#tag/comments/paths/~1delete_comment~1{id}/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Splitwise comment ID to delete. |
