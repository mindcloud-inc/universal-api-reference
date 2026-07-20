# Complete Replenishment with Synchroteam

Completes a replenishment request in Synchroteam.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Api/v2/StockRequest/Complete`
- **Base URL:** `https://ws.synchroteam.com`
- **Official documentation:** [Complete Replenishment](https://api.synchroteam.com/v2/#complete-a-replenishment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload` | body | `object` | yes | Request body payload for completing a stock request (per docs). |
