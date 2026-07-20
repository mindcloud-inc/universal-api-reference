# Get Shipment Document with Shipcloud

Retrieves a shipment document from Shipcloud by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/shipments/:shipmentId/shipment_documents/:shipmentDocumentId`
- **Base URL:** `https://api.shipcloud.io/v1`
- **Official documentation:** [Get Shipment Document](https://developers.shipcloud.io/swagger-ui/#/default/get_shipments__shipment_id__shipment_documents__shipment_document_id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipment_document_id` | path | `string` | yes | The Shipcloud shipment document identifier. |
| `shipment_id` | path | `string` | yes | The Shipcloud shipment identifier. |
