# Search Preset Transformations with Dash.app

Finds preset transformations in Dash.app by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/preset-transformation-searches`
- **Base URL:** `https://api-v2.dash.app`
- **Official documentation:** [Search Preset Transformations](https://api-docs.dash.app/dash/openapi/preset-transformations/postpresettransformationsearch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `criterion` | body | `object` | yes | Preset transformation search criterion object. |
| `from` | body | `number` | yes | Zero-based result offset. |
| `pageSize` | body | `number` | yes | Maximum number of results to return. |
| `sorts[]` | body | `array<object>` | no | Array of preset transformation sort objects. |
