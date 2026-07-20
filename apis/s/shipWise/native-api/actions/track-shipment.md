# Track Shipment with ShipWise

Retrieves shipment tracking details from ShipWise.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/Ship/Tracking`
- **Base URL:** `https://api.shipwise.com/`
- **Official documentation:** [Track Shipment](https://api.shipwise.com/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TrackingNumber` | query | `string` | no | Carrier tracking number to look up. Provide this or Package ID. |
| `packageid` | query | `string` | no | ShipWise package ID to look up. Provide this or Tracking Number. |
