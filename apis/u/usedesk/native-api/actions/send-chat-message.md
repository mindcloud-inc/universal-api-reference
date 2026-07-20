# Send Chat Message with Usedesk

Sends a chat message in Usedesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/sendMessage`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [Send Chat Message](https://api.usedocs.com/article/51395)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | body | `number` | yes | Chat ID. |
| `user_id` | body | `number` | yes | Agent ID on whose behalf the message will be sent. |
| `text` | body | `string` | yes | Message text. |
