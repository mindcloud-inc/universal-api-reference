# Delete Live Stream Playback ID with Mux

## Endpoint

- **Method:** `DELETE`
- **Path:** `/video/v1/live-streams/{LIVE_STREAM_ID}/playback-ids/{PLAYBACK_ID}`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Delete Live Stream Playback ID](https://www.mux.com/docs/api-reference/video/live-streams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `LIVE_STREAM_ID` | path | `string` | yes | The Mux live stream ID. |
| `PLAYBACK_ID` | path | `string` | yes | The Mux playback ID. |
