# Update Asset Master Access with Mux

## Endpoint

- **Method:** `PUT`
- **Path:** `/video/v1/assets/{ASSET_ID}/master-access`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Update Asset Master Access](https://www.mux.com/docs/api-reference/video/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ASSET_ID` | path | `string` | yes | The Mux asset ID. |
| `master_access` | body | `string` | yes | Controls master access generation. |
