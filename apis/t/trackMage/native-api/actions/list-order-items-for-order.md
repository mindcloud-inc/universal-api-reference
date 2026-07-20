# List Order Items For Order with TrackMage

Retrieves order items for an order in TrackMage.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/{id}/items`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [List Order Items For Order](https://docs.trackmage.com/docs/order/order-item.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Order identifier |
| `page` | query | `number` | no | The collection page number |
| `itemsPerPage` | query | `number` | no | The number of items per page |
