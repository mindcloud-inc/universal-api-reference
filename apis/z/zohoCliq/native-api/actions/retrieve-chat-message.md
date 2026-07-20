# Retrieve Chat Message with Zoho Cliq

Retrieves a chat message from Zoho Cliq by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats/:chatId/messages/:messageId`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [Retrieve Chat Message](https://www.zoho.com/cliq/help/restapi/v2/#Retrieve_Message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The ID of the chat containing the message. |
| `messageId` | path | `string` | yes | The ID of the message to retrieve. |
