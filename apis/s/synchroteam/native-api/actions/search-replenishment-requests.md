# Search Replenishment Requests with Synchroteam

Finds replenishment requests in Synchroteam using supported filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/v2/StockRequest/Search`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Search Replenishment Requests](https://api.synchroteam.com/v2/#search-replenishment-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | Optional. Provide the Synchroteam stock request search filters object (per docs). |
