# Get Message with Blooio Messaging

Retrieves a message from Blooio Messaging.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats/{chatId}/messages/{messageId}`
- **Base URL:** `https://backend.blooio.com/v2/api`
- **Official documentation:** [Get Message](https://docs.blooio.com/messages/getMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | Chat identifier. Use a phone number, email, group ID, or comma-separated recipient list. |
| `messageId` | path | `string` | yes | Message identifier. |
