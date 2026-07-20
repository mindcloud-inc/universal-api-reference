# List Chat Messages with Zoho Cliq

Retrieves messages from a Zoho Cliq chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats/:chatId/messages`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [List Chat Messages](https://www.zoho.com/cliq/help/restapi/v2/#Get_Messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The ID of the chat whose messages should be retrieved. |
| `fromtime` | query | `number` | no | Retrieve messages sent after this time in milliseconds. |
| `totime` | query | `number` | no | Retrieve messages sent before this time in milliseconds. |
| `limit` | query | `number` | no | The number of messages to retrieve. Default and maximum is 100. |
