# Get Ticket By Barcode with Ticketbud

Finds a ticket in Ticketbud by barcode.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/tickets/:barcode.json`
- **Base URL:** `https://api.ticketbud.com`
- **Official documentation:** [Get Ticket By Barcode](https://api.ticketbud.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | The Ticketbud event ID that owns the ticket. |
| `barcode` | path | `string` | yes | The Ticketbud ticket barcode to retrieve. |
