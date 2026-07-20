# Create Comment with Splitwise

Creates a new expense comment in Splitwise.

## Endpoint

- **Method:** `POST`
- **Path:** `/create_comment`
- **Base URL:** `https://secure.splitwise.com/api/v3.0`
- **Official documentation:** [Create Comment](https://dev.splitwise.com/#tag/comments/paths/~1create_comment/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Comment text to add to the expense. |
| `expense_id` | body | `number` | yes | Splitwise expense ID to comment on. |
