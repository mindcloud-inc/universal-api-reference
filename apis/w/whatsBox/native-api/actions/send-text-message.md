# Send Text Message with WhatsBox

Sends a text message from WhatsBox within the 24-hour window.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/text`
- **Base URL:** `https://api.whatsbox.io`
- **Official documentation:** [Send Text Message](https://api.whatsbox.io/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | body | `string` | yes | Channel ID for your WhatsApp number. |
| `to` | body | `string` | yes | Recipient phone number. |
| `name` | body | `string` | no | Recipient name when creating a new contact. |
| `user_id` | body | `string` | no | Team member ID to show as sender. |
| `medium` | body | `string` | no | Platform or application name. |
| `body` | body | `string` | yes | Text message body. |
| `preview_url` | body | `boolean` | no | Whether WhatsApp should generate link previews. |
