# Get inventory adjustments with Fraser Direct

## Endpoint

- **Method:** `GET`
- **Path:** `/GetInventoryAdjustments`
- **Base URL:** `{baseURL}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `StartDateTimeGMT` | body | `string` | yes | Required UTC timestamp in yyyy-MM-ddTHH:mm:ss format. |
| `EndDateTimeGMT` | body | `string` | no | Optional UTC timestamp in yyyy-MM-ddTHH:mm:ss format. When omitted, Fraser Direct returns all adjustments on or after StartDateTimeGMT. |
