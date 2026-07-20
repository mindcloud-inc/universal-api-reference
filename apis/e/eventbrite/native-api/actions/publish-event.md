# Publish Event with Eventbrite

Publishes an event in Eventbrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/:eventId/publish/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [Publish Event](https://www.eventbrite.com/platform/docs/create-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Event identifier. |
