# Create Event Recording Download URL with Restream

Generates a download URL for an event recording in Restream.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/events/:eventId/recordings/download-url`
- **Base URL:** `https://api.restream.io/v2`
- **Official documentation:** [Create Event Recording Download URL](https://developers.restream.io/events/events-recording-download-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The UUID of the event whose recording download URL to generate. |
| `fileName` | body | `string` | yes | The file name from the event recordings response. |
