# Create Batch of Labels with Easyship

Creates a batch of shipment labels in Easyship.

## Endpoint

- **Method:** `POST`
- **Path:** `/batches/labels`
- **Base URL:** `https://public-api.easyship.com/2024-09`
- **Official documentation:** [Create Batch of Labels](https://developers.easyship.com/reference/batch_labels_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipments[]` | body | `array<object>` | yes | Shipments to confirm and label. |
| `shipments[].easyship_shipment_id` | body | `string` | yes | Existing Easyship shipment ID to label. |
| `shipments[].courier_service_id` | body | `string` | no | Optional courier service override for this shipment. |
