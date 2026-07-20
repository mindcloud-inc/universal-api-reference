# Update a live stream with api.video

Updates an existing live stream in api.video.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/live-streams/:liveStreamId`
- **Base URL:** `https://ws.api.video`
- **Official documentation:** [Update a live stream](https://docs.api.video/reference/api/Live-Streams#update-a-live-stream)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `liveStreamId` | path | `string` | yes | The unique identifier for the live stream. |
| `name` | body | `string` | no | Optional updated display name for the live stream. |
