# Generate Asset Track Subtitles with Mux

## Endpoint

- **Method:** `POST`
- **Path:** `/video/v1/assets/{ASSET_ID}/tracks/{TRACK_ID}/generate-subtitles`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Generate Asset Track Subtitles](https://www.mux.com/docs/api-reference/video/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ASSET_ID` | path | `string` | yes | The Mux asset ID. |
| `generated_subtitles[]` | body | `array<object>` | yes | Generated subtitle definitions. |
| `TRACK_ID` | path | `string` | yes | The Mux track ID. |
