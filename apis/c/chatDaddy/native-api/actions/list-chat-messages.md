# List Chat Messages with ChatDaddy

Retrieves messages from a chat in ChatDaddy.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/{accountId}/{chatId}`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [List Chat Messages](https://chatdaddy.stoplight.io/docs/openapi/65b9cd3fc76e9-fetch-messages-of-the-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Account identifier for the chat. |
| `chatId` | path | `string` | yes | Chat identifier to fetch messages for. |
