# Retrieve Asset Playback ID with Mux

## Endpoint

- **Method:** `GET`
- **Path:** `/video/v1/assets/{ASSET_ID}/playback-ids/{PLAYBACK_ID}`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Retrieve Asset Playback ID](https://www.mux.com/docs/api-reference/video/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ASSET_ID` | path | `string` | yes | The Mux asset ID. |
| `PLAYBACK_ID` | path | `string` | yes | The Mux playback ID. |
