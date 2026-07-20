# Delete Asset Static Rendition with Mux

## Endpoint

- **Method:** `DELETE`
- **Path:** `/video/v1/assets/{ASSET_ID}/static-renditions/{STATIC_RENDITION_ID}`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Delete Asset Static Rendition](https://www.mux.com/docs/api-reference/video/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ASSET_ID` | path | `string` | yes | The Mux asset ID. |
| `STATIC_RENDITION_ID` | path | `string` | yes | The static rendition ID. |
