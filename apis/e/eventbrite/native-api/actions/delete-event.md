# Delete Event with Eventbrite

Deletes an existing event from Eventbrite.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/events/:eventId/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [Delete Event](https://www.eventbrite.com/platform/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Event identifier. |
