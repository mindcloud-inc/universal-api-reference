# Get Event Stream Key with Restream

Retrieves an event stream key from Restream.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/events/:eventId/streamKey`
- **Base URL:** `https://api.restream.io/v2`
- **Official documentation:** [Get Event Stream Key](https://developers.restream.io/events/event-stream-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The UUID of the event whose stream key to retrieve. |
