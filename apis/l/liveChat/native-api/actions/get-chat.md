# Get Chat with LiveChat

Retrieves a chat with thread details from LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/get_chat`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Get Chat](https://platform.text.com/docs/messaging/agent-chat-api#get-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | body | `string` | yes | The ID of the chat to fetch. |
| `thread_id` | body | `string` | no | The thread ID to fetch. Defaults to the latest thread if omitted. |
