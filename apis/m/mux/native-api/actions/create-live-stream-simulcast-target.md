# Create Live Stream Simulcast Target with Mux

## Endpoint

- **Method:** `POST`
- **Path:** `/video/v1/live-streams/{LIVE_STREAM_ID}/simulcast-targets`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Create Live Stream Simulcast Target](https://www.mux.com/docs/api-reference/video/live-streams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `LIVE_STREAM_ID` | path | `string` | yes | The Mux live stream ID. |
| `url` | body | `string` | yes | The RTMP destination URL for the simulcast target. |
