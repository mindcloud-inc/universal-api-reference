# Delete Chat Message with Zoho Cliq

Deletes an existing chat message from Zoho Cliq.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/chats/:chatId/messages/:messageId`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [Delete Chat Message](https://www.zoho.com/cliq/help/restapi/v2/#Delete_Message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The ID of the chat containing the message. |
| `messageId` | path | `string` | yes | The ID of the message to delete. |
