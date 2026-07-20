# Get Shipment with Kladana

Retrieves a shipment record from Kladana.

## Endpoint

- **Method:** `GET`
- **Path:** `/entity/demand/{id}`
- **Base URL:** `https://api.kladana.com/api/remap/1.2`
- **Official documentation:** [Get Shipment](https://dev.kladana.com/doc/api/remap/1.2/documents/#transactions-shipment-get-shipment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Kladana shipment ID from the Shipment resource URL. |
