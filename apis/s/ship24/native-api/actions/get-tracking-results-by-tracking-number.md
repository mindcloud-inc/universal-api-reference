# Get Tracking Results by Tracking Number with Ship24

Retrieves tracking results by tracking number from Ship24.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/tracking/search`
- **Base URL:** `https://api.ship24.com`
- **Official documentation:** [Get Tracking Results by Tracking Number](https://docs.ship24.com/tracking-api-reference/#/operations/get-tracking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackingNumber` | body | `string` | yes | Tracking number of the shipment. |
