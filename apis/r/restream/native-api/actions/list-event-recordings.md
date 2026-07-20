# List Event Recordings with Restream

Retrieves event recordings from Restream.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/events/:eventId/recordings`
- **Base URL:** `https://api.restream.io/v2`
- **Official documentation:** [List Event Recordings](https://developers.restream.io/events/events-recordings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The UUID of the event whose recordings to list. |
