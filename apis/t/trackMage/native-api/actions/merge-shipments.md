# Merge Shipments with TrackMage

Merges shipments into one shipment in TrackMage.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipments/merge`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [Merge Shipments](https://docs.trackmage.com/docs/shipment/shipment.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | body | `string` | no |
| `trackingNumber` | body | `string` | no |
| `shipmentId` | body | `string` | no |
