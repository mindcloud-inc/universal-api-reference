# Create Message with GrooveHQ

Creates a new message in a GrooveHQ ticket.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:ticketNumber/messages`
- **Base URL:** `https://api.groovehq.com/v1`
- **Official documentation:** [Create Message](https://doc.groovehq.com/messages)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ticketNumber` | path | `string` | yes |
| `body` | body | `string` | yes |
| `author` | body | `string` | no |
| `sent_at` | body | `date` | no |
| `note` | body | `boolean` | no |
| `send_copy_to_customer` | body | `boolean` | no |
| `skip_unread_ticket` | body | `boolean` | no |
| `skip_notifications` | body | `boolean` | no |
