# Create Event Ticket Class with Eventbrite

Creates a new event ticket class in Eventbrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/:eventId/ticket_classes/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [Create Event Ticket Class](https://www.eventbrite.com/platform/docs/create-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Event identifier. |
| `ticket_class.free` | body | `boolean` | yes | Whether this ticket class is free. |
| `ticket_class.name` | body | `string` | yes | Ticket class display name. |
| `ticket_class.quantity_total` | body | `number` | yes | Total quantity for this ticket class. |
