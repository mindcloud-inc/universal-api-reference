# Send Message with Blooio Messaging

Sends a message in a Blooio Messaging chat.

## Endpoint

- **Method:** `POST`
- **Path:** `/chats/{chatId}/messages`
- **Base URL:** `https://backend.blooio.com/v2/api`
- **Official documentation:** [Send Message](https://docs.blooio.com/messages/sendMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | Chat identifier. Use a valid E.164 phone number, email, group ID, or comma-separated recipient list. |
| `text` | body | `string` | no | Message text. |
