# Update Shipment with Flexport

Updates an existing shipment in Flexport.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/shipments/:id`
- **Base URL:** `https://api.flexport.com`
- **Official documentation:** [Update Shipment](https://apidocs.flexport.com/2023-07-01/tag/Shipment#operation/shipment_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique Flexport shipment ID to update. |
| `metadata` | body | `object` | no | Metadata object to replace existing shipment metadata. Keys should be strings and values should be arrays. |
