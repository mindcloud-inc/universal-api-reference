# List Shipment Documents with Shipcloud

Retrieves shipment documents from Shipcloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/shipments/:shipmentId/shipment_documents`
- **Base URL:** `https://api.shipcloud.io/v1`
- **Official documentation:** [List Shipment Documents](https://developers.shipcloud.io/swagger-ui/#/default/get_shipments__shipment_id__shipment_documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipment_id` | path | `string` | yes | The Shipcloud shipment identifier. |
