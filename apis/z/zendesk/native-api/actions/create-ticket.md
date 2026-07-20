# Create Ticket with Zendesk

Creates a new ticket in Zendesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Create Ticket](https://developer.zendesk.com/api-reference/ticketing/tickets/tickets/#create-ticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticket.comment.body` | body | `string` | yes | Initial ticket comment. |
| `ticket.subject` | body | `string` | no | Ticket subject line. |
| `ticket.priority` | body | `string` | no | Ticket priority (low, normal, high, urgent). Accepted values: `0`, `1`, `2`, `3`. |
| `ticket.status` | body | `string` | no | Ticket status (new, open, pending, hold, solved, closed). |
