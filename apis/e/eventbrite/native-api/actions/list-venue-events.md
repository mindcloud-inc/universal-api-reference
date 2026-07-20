# List Venue Events with Eventbrite

Retrieves venue events from Eventbrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/venues/:venueId/events/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [List Venue Events](https://www.eventbrite.com/platform/api#/reference/event/list/list-events-by-venue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `venueId` | path | `string` | yes | Venue identifier. |
