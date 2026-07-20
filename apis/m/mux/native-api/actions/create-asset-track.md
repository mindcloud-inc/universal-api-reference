# Create Asset Track with Mux

## Endpoint

- **Method:** `POST`
- **Path:** `/video/v1/assets/{ASSET_ID}/tracks`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Create Asset Track](https://www.mux.com/docs/api-reference/video/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ASSET_ID` | path | `string` | yes | The Mux asset ID. |
| `language_code` | body | `string` | yes | The BCP-47 language code. |
| `type` | body | `string` | yes | The track type. |
| `url` | body | `string` | yes | The public URL for the track file. |
