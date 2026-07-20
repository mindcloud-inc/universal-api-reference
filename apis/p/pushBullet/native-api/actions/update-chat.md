# Update Chat with Pushbullet

Updates an existing chat in Pushbullet.

## Endpoint

- **Method:** `POST`
- **Path:** `/chats/:chat_iden`
- **Base URL:** `https://api.pushbullet.com/v2`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_iden` | path | `string` | yes | Chat identifier to update. |
| `muted` | body | `boolean` | yes | Set true to mute the chat and false to unmute. |
