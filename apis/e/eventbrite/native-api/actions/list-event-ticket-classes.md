# List Event Ticket Classes with Eventbrite

Retrieves event ticket classes from Eventbrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/ticket_classes/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [List Event Ticket Classes](https://www.eventbrite.com/platform/docs/create-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Event identifier. |
