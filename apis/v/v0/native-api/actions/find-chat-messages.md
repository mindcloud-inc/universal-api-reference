# Find Chat Messages with v0

Finds messages in a v0 chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/chats/:chatId/messages`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Find Chat Messages](https://v0.app/docs/api/platform/reference/chats/find-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The ID of the chat whose messages to list. |
| `limit` | query | `number` | no | Specifies the maximum number of message records to return in a single response. |
| `cursor` | query | `string` | no | Base64 encoded cursor containing pagination data. |
