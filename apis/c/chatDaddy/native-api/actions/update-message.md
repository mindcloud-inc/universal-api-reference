# Update Message with ChatDaddy

Updates an existing message or note in ChatDaddy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/messages/{accountId}/{chatId}/{id}`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [Update Message](https://chatdaddy.stoplight.io/docs/openapi/d322f828da052-modify-a-message-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Account identifier for the message. |
| `chatId` | path | `string` | yes | Chat identifier for the message. |
| `id` | path | `string` | yes | Message identifier to update. |
