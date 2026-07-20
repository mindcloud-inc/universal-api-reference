# List Conversations with Dify

Retrieves conversations from Dify.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [List Conversations](https://docs.dify.ai/api-reference/conversations/list-conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | query | `string` | no | User identifier. |
| `last_id` | query | `string` | no | Cursor for the next page of conversations. |
| `sort_by` | query | `string` | no | Sort order for conversations. |
