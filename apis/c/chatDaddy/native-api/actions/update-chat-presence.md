# Update Chat Presence with ChatDaddy

Updates a chat's presence in ChatDaddy.

## Endpoint

- **Method:** `POST`
- **Path:** `/chats/{accountId}/{id}/presence`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [Update Chat Presence](https://chatdaddy.stoplight.io/docs/openapi/60a7396ac5198-update-a-chat-s-presence)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Account identifier for the chat. |
| `id` | path | `string` | yes | Chat identifier to update presence for. |
| `presence` | query | `string` | yes | Presence state to publish for the chat. |
