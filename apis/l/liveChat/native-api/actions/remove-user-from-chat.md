# Remove User From Chat with LiveChat

Updates a chat by removing a user in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/remove_user_from_chat`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Remove User From Chat](https://platform.text.com/docs/messaging/agent-chat-api#remove-user-from-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | body | `string` | yes | The target chat ID. |
| `user_id` | body | `string` | yes | The user ID to remove. |
| `user_type` | body | `string` | yes | Possible values: agent. |
| `ignore_requester_presence` | body | `boolean` | no | Allow the action even if the requester is not on the chat user list. |
