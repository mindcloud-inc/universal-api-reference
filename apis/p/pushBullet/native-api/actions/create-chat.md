# Create Chat with Pushbullet

Creates a new chat in Pushbullet.

## Endpoint

- **Method:** `POST`
- **Path:** `/chats`
- **Base URL:** `https://api.pushbullet.com/v2`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Recipient email for the chat. |
| `muted` | body | `boolean` | no | Set true to mute the chat after creation. |
