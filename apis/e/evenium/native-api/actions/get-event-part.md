# Get Event Part with Evenium

Retrieves an event part from Evenium.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/eventParts/:eventPartId`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [Get Event Part](https://static.evenium.com/api-docs/organizer/index-json.html#_get_event_part)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `number` | yes | The Evenium eventId. |
| `eventPartId` | path | `number` | yes | The Evenium eventPartId. |
