# Delete Conversation with Dify

Deletes an existing conversation from Dify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/conversations/:conversation_id`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Delete Conversation](https://docs.dify.ai/api-reference/conversations/delete-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID to delete. |
| `user` | body | `string` | no | User identifier. |
