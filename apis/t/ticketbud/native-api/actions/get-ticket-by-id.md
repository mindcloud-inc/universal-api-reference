# Get Ticket By ID with Ticketbud

Retrieves a ticket from Ticketbud by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/tickets/:id.json`
- **Base URL:** `https://api.ticketbud.com`
- **Official documentation:** [Get Ticket By ID](https://api.ticketbud.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | The Ticketbud event ID that owns the ticket. |
| `id` | path | `string` | yes | The Ticketbud ticket ID to retrieve. |
