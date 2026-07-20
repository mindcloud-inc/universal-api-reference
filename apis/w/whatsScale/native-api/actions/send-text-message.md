# Send Text Message with WhatsScale

Sends a text message through WhatsScale.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/sendText`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Send Text Message](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | body | `string` | yes | Recipient chat ID, such as 31612345678@c.us or a group/channel ID. |
| `session` | body | `string` | yes | Session name from /api/sessions. |
| `text` | body | `string` | yes | Message text, up to 4096 characters. |
