# Update Asset MP4 Support with Mux

## Endpoint

- **Method:** `PUT`
- **Path:** `/video/v1/assets/{ASSET_ID}/mp4-support`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Update Asset MP4 Support](https://www.mux.com/docs/api-reference/video/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ASSET_ID` | path | `string` | yes | The Mux asset ID. |
| `mp4_support` | body | `string` | yes | Controls MP4 support generation. |
