# Create Note with Freshdesk

Creates a note on a Freshdesk ticket.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:ticketId/notes`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [Create Note](https://developers.freshdesk.com/api/#add_note_to_a_ticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | path | `list<number>` | yes | Freshdesk ticket ID. |
| `attachments[]` | body | `array<object>` | no | Note attachments |
| `body` | body | `string` | no | Note content in HTML |
| `structured_body` | body | `object` | no | Structured content body for the note |
| `incoming` | body | `boolean` | no | Mark note as incoming external activity |
| `notify_emails[]` | body | `array<string>` | no | Emails to notify about this note |
| `private` | body | `boolean` | no | Whether the note is private |
| `user_id` | body | `list<number>` | no | Agent/user ID adding the note |
