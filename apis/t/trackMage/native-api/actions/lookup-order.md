# Lookup Order with TrackMage

Finds an order in TrackMage by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/lookup`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [Lookup Order](https://docs.trackmage.com/docs/order/order.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | body | `string` | no |
| `search` | body | `string` | no |
| `shipmentId` | body | `string` | no |
