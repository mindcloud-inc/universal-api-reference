# List Chats with ChatDaddy

Retrieves chat records from your ChatDaddy account.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [List Chats](https://chatdaddy.stoplight.io/docs/openapi/b6ddd4eb5d04b-get-chats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Number of chats to return. |
| `page` | query | `string` | no | Cursor for the next chat page. |
