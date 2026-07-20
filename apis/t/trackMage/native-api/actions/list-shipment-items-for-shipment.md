# List Shipment Items For Shipment with TrackMage

Retrieves shipment items for a shipment in TrackMage.

## Endpoint

- **Method:** `GET`
- **Path:** `/shipments/{id}/shipment_items`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [List Shipment Items For Shipment](https://docs.trackmage.com/docs/shipment/shipment-item.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Shipment identifier |
| `page` | query | `number` | no | The collection page number |
| `itemsPerPage` | query | `number` | no | The number of items per page |
