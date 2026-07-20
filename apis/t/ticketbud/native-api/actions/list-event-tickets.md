# List Event Tickets with Ticketbud

Retrieves event tickets from Ticketbud.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/tickets.json`
- **Base URL:** `https://api.ticketbud.com`
- **Official documentation:** [List Event Tickets](https://api.ticketbud.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | The Ticketbud event ID to list tickets for. |
