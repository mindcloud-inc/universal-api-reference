# Update Live Stream New Asset Static Renditions with Mux

## Endpoint

- **Method:** `PUT`
- **Path:** `/video/v1/live-streams/{LIVE_STREAM_ID}/new-asset-settings/static-renditions`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Update Live Stream New Asset Static Renditions](https://www.mux.com/docs/api-reference/video/live-streams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `static_renditions[]` | body | `array<object>` | yes | Static rendition settings for new assets. |
