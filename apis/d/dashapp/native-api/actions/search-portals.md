# Search Portals with Dash.app

Finds portals in Dash.app by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/portal-searches`
- **Base URL:** `https://api-v2.dash.app`
- **Official documentation:** [Search Portals](https://api-docs.dash.app/dash/openapi/portals/postportalsearch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `criterion` | body | `object` | yes | Portal search criterion object. |
| `from` | body | `number` | yes | Zero-based result offset. |
| `pageSize` | body | `number` | yes | Maximum number of results to return. |
| `sorts[]` | body | `array<object>` | yes | Array of portal sort objects. |
