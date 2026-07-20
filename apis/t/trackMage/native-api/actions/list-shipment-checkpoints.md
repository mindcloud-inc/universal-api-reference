# List Shipment Checkpoints with TrackMage

Retrieves shipment checkpoints for a shipment in TrackMage.

## Endpoint

- **Method:** `GET`
- **Path:** `/shipments/{id}/checkpoints`
- **Base URL:** `https://api.trackmage.com/`
- **Official documentation:** [List Shipment Checkpoints](https://docs.trackmage.com/docs/shipment/tracking-checkpoint.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Shipment identifier |
| `page` | query | `number` | no | The collection page number |
| `itemsPerPage` | query | `number` | no | The number of items per page |
