# Send Message with ChatDaddy

Sends a message to a ChatDaddy chat.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/{accountId}/{chatId}`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [Send Message](https://chatdaddy.stoplight.io/docs/openapi/5f6bdc0458e27-send-a-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Account identifier to send from. |
| `chatId` | path | `string` | yes | Chat identifier to send the message to. |
| `text` | body | `string` | yes | Message text content. |
