# Send Chat Message with Dify

Creates a chat message in Dify.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat-messages`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Send Chat Message](https://docs.dify.ai/api-reference/chats/send-chat-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | User input or question content. |
| `inputs` | body | `object` | yes | App input variables as key/value pairs. |
| `response_mode` | body | `string` | no | Response mode: streaming or blocking. |
| `user` | body | `string` | yes | User identifier, unique within the application. |
| `conversation_id` | body | `string` | no | Conversation ID to continue an existing conversation. |
| `files` | body | `list<object>` | no | Files for multimodal understanding. |
| `auto_generate_name` | body | `boolean` | no | Whether to auto-generate the conversation title. |
| `workflow_id` | body | `string` | no | Published workflow version ID to execute. |
