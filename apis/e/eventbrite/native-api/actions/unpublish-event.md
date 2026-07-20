# Unpublish Event with Eventbrite

Unpublishes an event in Eventbrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/:eventId/unpublish/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [Unpublish Event](https://www.eventbrite.com/platform/docs/create-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Event identifier. |
