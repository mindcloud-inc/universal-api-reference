# Send Rich Message Postback with LiveChat

Sends a rich message postback in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/send_rich_message_postback`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Send Rich Message Postback](https://platform.text.com/docs/messaging/agent-chat-api#send-rich-message-postback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | body | `string` | yes | The chat ID. |
| `event_id` | body | `string` | yes | The rich message event ID. |
| `postback` | body | `object` | yes | The postback payload. |
| `postback.id` | body | `string` | yes | The postback name of the button. |
| `postback.toggled` | body | `boolean` | yes | Whether the postback is toggled. |
| `thread_id` | body | `string` | yes | The thread ID. |
