# Send Media Message with WhatsBox

Sends a media message from WhatsBox within the 24-hour window.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/media`
- **Base URL:** `https://api.whatsbox.io`
- **Official documentation:** [Send Media Message](https://api.whatsbox.io/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | body | `string` | yes | Channel ID for your WhatsApp number. |
| `to` | body | `string` | yes | Recipient phone number. |
| `name` | body | `string` | no | Recipient name when creating a new contact. |
| `user_id` | body | `string` | no | Team member ID to show as sender. |
| `medium` | body | `string` | no | Platform or application name. |
| `type` | body | `string` | yes | Media type. |
| `link` | body | `string` | yes | Public media URL. |
| `caption` | body | `string` | no | Media caption. |
| `filename` | body | `string` | no | Document filename. |
