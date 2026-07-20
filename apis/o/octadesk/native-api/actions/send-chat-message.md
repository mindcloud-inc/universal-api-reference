# Send Chat Message with Octadesk

Creates a message in an Octadesk chat.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/:id/messages`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Send Chat Message](https://developers.octadesk.com/reference/sendmessagetochat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | Message content. |
| `channel` | body | `string` | yes | Channel that this message is from. |
| `chatId` | body | `string` | yes | ID of the chat that this message will be included. |
| `id` | path | `string` | yes | Chat ID from Octadesk. |
| `type` | body | `string` | yes | Whether the message is intended for public or internal communication. |
