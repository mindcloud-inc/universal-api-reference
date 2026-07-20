# List Conversation Messages with Dify

Retrieves conversation messages from Dify.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [List Conversation Messages](https://docs.dify.ai/api-reference/conversations/list-conversation-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | query | `string` | yes | Conversation ID to list messages for. |
| `user` | query | `string` | no | User identifier. |
| `first_id` | query | `string` | no | Cursor for loading older messages. |
