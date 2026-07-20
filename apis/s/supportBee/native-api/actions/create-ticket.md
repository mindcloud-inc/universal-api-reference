# Create Ticket with SupportBee

Creates a new ticket in SupportBee.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Create Ticket](https://supportbee.com/docs/api/reference#tag/Tickets/paths/~1tickets/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket.subject` | body | `string` | yes | Ticket subject line. |
| `ticket.requester_name` | body | `string` | no | Requester display name. |
| `ticket.requester_email` | body | `string` | yes | Requester email address. |
| `ticket.notify_requester` | body | `boolean` | no | Whether to notify the requester on create. |
| `ticket.content.text` | body | `string` | yes | Plain-text ticket body. |
