# Update Event with Eventbrite

Updates an existing event in Eventbrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/:eventId/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [Update Event](https://www.eventbrite.com/platform/docs/create-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event.name.html` | body | `string` | yes | Updated event title. |
| `eventId` | path | `string` | yes | Event identifier. |
