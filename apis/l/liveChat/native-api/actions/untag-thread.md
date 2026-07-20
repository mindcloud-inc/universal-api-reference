# Untag Thread with LiveChat

Updates a thread by untagging it in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/untag_thread`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Untag Thread](https://platform.text.com/docs/messaging/agent-chat-api#untag-thread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | body | `string` | yes | The chat ID. |
| `thread_id` | body | `string` | yes | The thread ID. |
| `tag` | body | `string` | yes | The tag name. Case sensitive. |
