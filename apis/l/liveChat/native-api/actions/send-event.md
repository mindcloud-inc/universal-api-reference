# Send Event with LiveChat

Sends a new event in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/send_event`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Send Event](https://platform.text.com/docs/messaging/agent-chat-api#send-event)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | body | `string` | yes | The chat ID to send an event to. |
| `event` | body | `object` | yes | The event payload to send. |
