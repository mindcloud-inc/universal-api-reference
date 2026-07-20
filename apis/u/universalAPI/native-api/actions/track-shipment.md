# Track Shipment with Universal API

Retrieves tracking statuses for a shipment from Universal API.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/shipment/track/id/{trackingId}/statuses`
- **Base URL:** `https://api.prod.universalapi.io`
- **Official documentation:** [Track Shipment](https://docs.universalapi.io/reference/track-shipment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackingId` | path | `string` | yes | Shipment tracking ID. |
