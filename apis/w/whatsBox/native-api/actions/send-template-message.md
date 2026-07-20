# Send Template Message with WhatsBox

Sends an approved template message from WhatsBox.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/template`
- **Base URL:** `https://api.whatsbox.io`
- **Official documentation:** [Send Template Message](https://api.whatsbox.io/docs#tag/messages/POST/messages/template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | body | `string` | yes | Channel ID for your WhatsApp number. |
| `to` | body | `string` | yes | Recipient phone number. |
| `name` | body | `string` | no | Recipient name when creating a new contact. |
| `user_id` | body | `string` | no | Team member ID to show as sender. |
| `medium` | body | `string` | no | Platform or application name. |
| `template_name` | body | `string` | yes | Approved WhatsApp template name. |
| `components[]` | body | `array<object>` | no | Template component parameters. |
