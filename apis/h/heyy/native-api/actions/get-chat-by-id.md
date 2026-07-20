# Get Chat by ID with Heyy

Retrieves a chat by ID from Heyy.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:channelId]/chats/:chatId`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Get Chat by ID](https://docs.heyy.io/api-reference/get-chat-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The Heyy channel ID. |
| `chatId` | path | `string` | yes | The Heyy chat ID. |
