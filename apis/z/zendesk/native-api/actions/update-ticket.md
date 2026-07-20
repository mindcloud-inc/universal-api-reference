# Update Ticket with Zendesk

Updates an existing ticket in Zendesk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tickets/:id.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Update Ticket](https://developer.zendesk.com/api-reference/ticketing/tickets/tickets/#update-ticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Zendesk ticket ID. |
| `ticket.subject` | body | `string` | no | Updated ticket subject. |
| `ticket.status` | body | `string` | no | Ticket status (new, open, pending, hold, solved, closed). Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `ticket.priority` | body | `string` | no | Ticket priority (low, normal, high, urgent). Accepted values: `0`, `1`, `2`, `3`. |
| `ticket.comment.body` | body | `string` | no | Comment to append while updating ticket. |
