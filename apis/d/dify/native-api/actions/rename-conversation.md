# Rename Conversation with Dify

Updates a conversation name in Dify.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:conversation_id/name`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Rename Conversation](https://docs.dify.ai/api-reference/conversations/rename-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID to rename. |
| `name` | body | `string` | no | New conversation name. |
| `auto_generate` | body | `boolean` | no | Automatically generate the conversation name. |
| `user` | body | `string` | yes | User identifier. |
