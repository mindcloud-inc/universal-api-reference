# Send Message with Superchat

Sends a message to a contact in Superchat.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [Send Message](https://developers.superchat.com/reference/createmessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to[]` | body | `array<object>` | yes | — |
| `from.channel_id` | body | `string` | yes | Unique identifier of the channel. Always bears prefix 'mc_' |
| `from.name` | body | `string` | no | — |
| `content` | body | `object` | yes | Use the media object to send images, videos, audio files or documents. You have to upload the file via POST `/files` first. |
| `in_reply_to` | body | `string` | no | Message ID of the message the newly sent message will be a reply to. Only supported for email. |
