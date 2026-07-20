# Update Chat Properties with LiveChat

Updates existing chat properties in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/update_chat_properties`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Update Chat Properties](https://platform.text.com/docs/messaging/agent-chat-api#update-chat-properties)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The chat ID. |
| `properties` | body | `object` | yes | The chat properties payload to set. |
