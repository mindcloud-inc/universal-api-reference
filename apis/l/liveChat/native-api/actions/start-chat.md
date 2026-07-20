# Start Chat with LiveChat

Creates a new chat in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/start_chat`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Start Chat](https://platform.text.com/docs/messaging/agent-chat-api#start-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat` | body | `object` | no | The chat payload to create. |
| `chat.properties` | body | `object` | no | Initial chat properties. |
| `chat.access` | body | `object` | no | Initial chat access settings. |
| `chat.users[]` | body | `array<object>` | no | Existing users to include in the chat. |
| `chat.users[].id` | body | `string` | yes | The user ID. |
| `chat.users[].type` | body | `string` | yes | Possible values: agent or customer. |
| `chat.thread` | body | `object` | no | The initial chat thread. |
| `chat.thread.events[]` | body | `array<object>` | no | Initial chat events. |
| `chat.thread.properties` | body | `object` | no | Initial thread properties. |
| `active` | body | `boolean` | no | Create an active thread by default. |
| `continuous` | body | `boolean` | no | Start the chat in continuous mode. |
