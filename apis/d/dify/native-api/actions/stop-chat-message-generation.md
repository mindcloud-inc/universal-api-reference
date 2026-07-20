# Stop Chat Message Generation with Dify

Stops chat message generation in Dify.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat-messages/:task_id/stop`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Stop Chat Message Generation](https://docs.dify.ai/api-reference/chats/stop-chat-message-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Streaming task ID to stop. |
| `user` | body | `string` | yes | User identifier used when the message was sent. |
