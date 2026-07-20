# Search Asset Download Events with Dash.app

Finds asset download events in Dash.app by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/asset-download-event-searches`
- **Base URL:** `https://api-v2.dash.app`
- **Official documentation:** [Search Asset Download Events](https://api-docs.dash.app/dash/openapi/asset-download-events/postassetdownloadeventsearch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `criterion` | body | `object` | yes |
| `from` | body | `number` | yes |
| `pageSize` | body | `number` | yes |
| `sorts[]` | body | `array<object>` | yes |
