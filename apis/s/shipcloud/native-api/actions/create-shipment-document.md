# Create Shipment Document with Shipcloud

Creates a new shipment document in Shipcloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipments/:shipmentId/shipment_documents`
- **Base URL:** `https://api.shipcloud.io/v1`
- **Official documentation:** [Create Shipment Document](https://developers.shipcloud.io/swagger-ui/#/default/post_shipments__shipment_id__shipment_documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipment_id` | path | `string` | yes | The Shipcloud shipment identifier. |
