# Get Event Sales Summary with Ticketbud

Retrieves an event sales summary from Ticketbud.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/ticket_sales`
- **Base URL:** `https://api.ticketbud.com`
- **Official documentation:** [Get Event Sales Summary](https://api.ticketbud.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | The Ticketbud event ID to retrieve sales summary for. |
