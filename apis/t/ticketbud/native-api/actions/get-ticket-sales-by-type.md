# Get Ticket Sales By Type with Ticketbud

Retrieves ticket sales by ticket type from Ticketbud.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/ticket_sales/:id.json`
- **Base URL:** `https://api.ticketbud.com`
- **Official documentation:** [Get Ticket Sales By Type](https://api.ticketbud.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | The Ticketbud event ID that owns the ticket type. |
| `id` | path | `string` | yes | The Ticketbud ticket type ID to retrieve sales for. |
