# Undo Ticket Check In with Ticketbud

Reverses a ticket check-in in Ticketbud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/events/:eventId/tickets/:id/check_in.json`
- **Base URL:** `https://api.ticketbud.com`
- **Official documentation:** [Undo Ticket Check In](https://api.ticketbud.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | The Ticketbud event ID that owns the ticket. |
| `id` | path | `string` | yes | The Ticketbud ticket ID to undo check-in for. |
