# Send Chat Message with Zoho Cliq

Creates a new chat message in Zoho Cliq.

## Endpoint

- **Method:** `POST`
- **Path:** `/chats/:chatId/message`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [Send Chat Message](https://www.zoho.com/cliq/help/restapi/v2/#Post_Message_Chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The ID of the chat where the message should be posted. |
| `text` | body | `string` | yes | The message text to post. |
| `reply_to` | body | `string` | no | The message ID to reply to. |
| `sync_message` | body | `boolean` | no | When true, post the message in a synchronous thread. |
| `mark_as_read` | body | `boolean` | no | When true, mark the sent message as read for the user. |
