# Retrieve Live Stream Simulcast Target with Mux

## Endpoint

- **Method:** `GET`
- **Path:** `/video/v1/live-streams/{LIVE_STREAM_ID}/simulcast-targets/{SIMULCAST_TARGET_ID}`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Retrieve Live Stream Simulcast Target](https://www.mux.com/docs/api-reference/video/live-streams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `LIVE_STREAM_ID` | path | `string` | yes | The Mux live stream ID. |
| `SIMULCAST_TARGET_ID` | path | `string` | yes | The simulcast target ID. |
