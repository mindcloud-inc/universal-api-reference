# List Expenses with Splitwise

Retrieves the current user's expenses from Splitwise.

## Endpoint

- **Method:** `GET`
- **Path:** `/get_expenses`
- **Base URL:** `https://secure.splitwise.com/api/v3.0`
- **Official documentation:** [List Expenses](https://dev.splitwise.com/#tag/expenses/paths/~1get_expenses/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dated_after` | query | `date` | no | Only return expenses dated after this timestamp. |
| `dated_before` | query | `date` | no | Only return expenses dated before this timestamp. |
| `friend_id` | query | `number` | no | Only return expenses involving this Splitwise user. |
| `group_id` | query | `number` | no | Only return expenses in this Splitwise group. |
| `limit` | query | `number` | no | Maximum number of expenses to return. |
| `offset` | query | `number` | no | Number of expenses to skip before returning results. |
| `updated_after` | query | `date` | no | Only return expenses updated after this timestamp. |
| `updated_before` | query | `date` | no | Only return expenses updated before this timestamp. |
