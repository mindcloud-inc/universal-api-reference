# List Upcoming Events with Restream

Retrieves upcoming events from Restream.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/events/upcoming`
- **Base URL:** `https://api.restream.io/v2`
- **Official documentation:** [List Upcoming Events](https://developers.restream.io/events/upcoming-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scheduled` | query | `boolean` | no | Filter for scheduled events. |
| `source` | query | `number` | no | Filter events by source type. |
