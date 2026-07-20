# List Event Attendees with Eventbrite

Retrieves event attendees from Eventbrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/attendees/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [List Event Attendees](https://www.eventbrite.com/platform/docs/attendees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Event identifier. |
