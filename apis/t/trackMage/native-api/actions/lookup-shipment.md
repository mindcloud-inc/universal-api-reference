# Lookup Shipment with TrackMage

Finds a shipment in TrackMage by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipments/lookup`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [Lookup Shipment](https://docs.trackmage.com/docs/shipment/shipment.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `search` | body | `string` | no |
| `orderId` | body | `string` | no |
| `workspaceId` | body | `string` | no |
