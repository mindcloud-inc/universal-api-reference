# Delete Message with ChatDaddy

Deletes an existing message from ChatDaddy.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/messages/{accountId}/{chatId}/{id}`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [Delete Message](https://chatdaddy.stoplight.io/docs/openapi/cb46687acadb3-delete-a-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Account identifier for the message. |
| `chatId` | path | `string` | yes | Chat identifier for the message. |
| `id` | path | `string` | yes | Message identifier to delete. |
