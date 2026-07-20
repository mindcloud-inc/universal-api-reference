# Create Asset Static Rendition with Mux

## Endpoint

- **Method:** `POST`
- **Path:** `/video/v1/assets/{ASSET_ID}/static-renditions`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Create Asset Static Rendition](https://www.mux.com/docs/api-reference/video/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ASSET_ID` | path | `string` | yes | The Mux asset ID. |
| `resolution` | body | `string` | yes | The static rendition resolution. |
