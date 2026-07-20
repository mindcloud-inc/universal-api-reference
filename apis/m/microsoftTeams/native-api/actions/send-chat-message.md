# Send Chat Message with Microsoft Teams

Creates a new chat message in Microsoft Teams.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/chats/:chatId/messages`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Send Chat Message](https://learn.microsoft.com/en-us/graph/api/chat-post-messages?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | Microsoft Graph chat ID. |
| `body.content` | body | `string` | yes | Chat message body content. |
