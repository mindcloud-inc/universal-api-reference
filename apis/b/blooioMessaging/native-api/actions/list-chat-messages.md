# List Chat Messages with Blooio Messaging

Retrieves messages from a Blooio Messaging chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats/{chatId}/messages`
- **Base URL:** `https://backend.blooio.com/v2/api`
- **Official documentation:** [List Chat Messages](https://docs.blooio.com/messages/listChatMessages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | Chat identifier. Use a phone number, email, group ID, or comma-separated recipient list. |
