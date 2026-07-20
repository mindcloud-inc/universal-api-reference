# Transfer Chat with LiveChat

Updates a chat by transferring it in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/transfer_chat`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Transfer Chat](https://platform.text.com/docs/messaging/agent-chat-api#transfer-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The chat ID. |
| `target` | body | `object` | no | Target transfer destination. |
| `target.type` | body | `string` | no | Possible values: group or agent. |
| `target.ids[]` | body | `array<string>` | no | Target group or agent IDs. |
| `ignore_agents_availability` | body | `boolean` | no | Allow the chat to be enqueued after transfer if needed. |
| `ignore_requester_presence` | body | `boolean` | no | Allow transfer even if the requester is not on the chat user list. |
