# Update Chat Message with Zoho Cliq

Updates an existing chat message in Zoho Cliq.

## Endpoint

- **Method:** `PUT`
- **Path:** `/chats/:chatId/messages/:messageId`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [Update Chat Message](https://www.zoho.com/cliq/help/restapi/v2/#Edit_Message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The ID of the chat containing the message. |
| `messageId` | path | `string` | yes | The ID of the message to edit. |
| `text` | body | `string` | yes | The updated message text. |
| `notify_edit` | body | `boolean` | no | When true, notify participants about the edited message. |
