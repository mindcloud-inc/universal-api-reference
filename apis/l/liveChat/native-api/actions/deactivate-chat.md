# Deactivate Chat with LiveChat

Updates a chat by deactivating it in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/deactivate_chat`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Deactivate Chat](https://platform.text.com/docs/messaging/agent-chat-api#deactivate-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The chat ID. |
| `ignore_requester_presence` | body | `boolean` | no | Allow the action even if the requester is not on the chat user list. |
