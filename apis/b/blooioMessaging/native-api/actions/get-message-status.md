# Get Message Status with Blooio Messaging

Retrieves a message status from Blooio Messaging.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats/{chatId}/messages/{messageId}/status`
- **Base URL:** `https://backend.blooio.com/v2/api`
- **Official documentation:** [Get Message Status](https://docs.blooio.com/messages/getMessageStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | Chat identifier. Use a phone number, email, group ID, or comma-separated recipient list. |
| `messageId` | path | `string` | yes | Message identifier. |
