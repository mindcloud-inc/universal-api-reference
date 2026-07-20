# Update Chat with ChatDaddy

Updates an existing chat in ChatDaddy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/chats/{accountId}/{id}`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [Update Chat](https://chatdaddy.stoplight.io/docs/openapi/5f76fa2ed242f-update-a-chat-read-unread-archive-pin-etc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Account identifier for the chat. |
| `action` | body | `string` | yes | Chat action to perform, such as read, unread, archive, or pin. |
| `id` | path | `string` | yes | Chat identifier to update. |
| `value` | body | `string` | yes | Value to apply for the selected chat action. |
