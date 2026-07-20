# Get Tracker Results By Tracking Number with Ship24

Retrieves tracker results by tracking number in Ship24.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v1/trackers/search/{trackingNumber}/results`
- **Base URL:** `https://api.ship24.com`
- **Official documentation:** [Get Tracker Results By Tracking Number](https://docs.ship24.com/tracking-api-reference/#/operations/get-tracking-results-of-trackers-by-tracking-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackingNumber` | path | `string` | yes | Tracking number of the shipment. |
