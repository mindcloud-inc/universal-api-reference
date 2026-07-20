# Add User To Chat with LiveChat

Updates a chat by adding a user in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/add_user_to_chat`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Add User To Chat](https://platform.text.com/docs/messaging/agent-chat-api#add-user-to-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | body | `string` | yes | The target chat ID. |
| `user_id` | body | `string` | yes | The user ID to add. |
| `user_type` | body | `string` | yes | Possible values: agent or customer. |
| `visibility` | body | `string` | yes | Possible values: all or agents. |
| `ignore_requester_presence` | body | `boolean` | no | Allow the action even if the requester is not on the chat user list. |
