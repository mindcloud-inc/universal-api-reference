# Send Conversation Message with SuperSend

Creates a message in a SuperSend conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/{id}/messages`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Send Conversation Message](https://docs.supersend.io/docs/conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `message` | body | `string` | yes | Message content (required for all platforms) |
| `sender_id` | body | `string` | no | Sender/mailbox ID to send from (required for email conversations). Must be an active sender in your organization. |
| `subject` | body | `string` | no | Email subject line (email only, defaults to "Re: {conversation title}") |
| `is_html` | body | `boolean` | no | Whether the message is HTML formatted (email only) Default: false. |
| `to` | body | `string` | no | Override recipient email address (email only, auto-selected if not provided) |
| `cc[]` | body | `array<string>` | no | CC recipients (email only) |
| `bcc[]` | body | `array<string>` | no | BCC recipients (email only) |
| `attachments[]` | body | `array<object>` | no | Email attachments (email only) |
