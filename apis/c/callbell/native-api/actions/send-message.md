# Send Message with Callbell

Creates a new outbound message in Callbell.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/send`
- **Base URL:** `https://api.callbell.eu/v1`
- **Official documentation:** [Send Message](https://docs.callbell.eu/api/reference/messages_api/post_send_messages/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assigned_user` | body | `string` | no | Collaborator email to assign to the message. |
| `bot_status` | body | `string` | no | Bot status to apply to the contact after sending. |
| `channel_uuid` | body | `string` | yes | Channel UUID to send the message from. |
| `content.text` | body | `string` | no | Text body for text messages. |
| `content.url` | body | `string` | no | Public URL for media messages. |
| `fields` | body | `string` | no | Comma-separated related resources to include in the response. |
| `from` | body | `string` | yes | Channel type such as whatsapp. |
| `metadata` | body | `object` | no | Metadata object to attach to the message. |
| `optin_contact` | body | `boolean` | no | Confirm that the contact opted in to receive messages. |
| `team_uuid` | body | `string` | no | Team UUID to assign to the message. |
| `template_uuid` | body | `string` | no | Template UUID for WhatsApp template messages. |
| `template_values[]` | body | `array<string>` | no | Template variable values in order. |
| `to` | body | `string` | yes | Destination phone number or platform identifier. |
| `type` | body | `string` | yes | Type of message to send. |
