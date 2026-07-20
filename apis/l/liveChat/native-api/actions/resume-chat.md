# Resume Chat with LiveChat

Restarts an archived chat in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/resume_chat`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Resume Chat](https://platform.text.com/docs/messaging/agent-chat-api#resume-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat` | body | `object` | yes | The chat payload to resume. |
| `chat.id` | body | `string` | yes | The ID of the chat to resume. |
| `chat.access` | body | `object` | no | Chat access to set. |
| `chat.properties` | body | `object` | no | Initial chat properties. |
| `chat.users[]` | body | `array<object>` | no | Existing users to include in the resumed chat. |
| `chat.users[].id` | body | `string` | yes | The user ID. |
| `chat.users[].type` | body | `string` | yes | Possible values: agent or customer. |
| `chat.thread` | body | `object` | no | The initial resumed chat thread. |
| `chat.thread.events[]` | body | `array<object>` | no | Initial chat events. |
| `chat.thread.properties` | body | `object` | no | Initial thread properties. |
| `active` | body | `boolean` | no | Create an active thread by default. |
| `continuous` | body | `boolean` | no | Leave chat continuous mode unchanged unless set. |
