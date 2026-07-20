# Create Shipment Form with EasyPost

Creates a new shipment form in EasyPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipments/:id/forms`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Create Shipment Form](https://docs.easypost.com/docs/shipments/forms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form` | body | `object` | yes | Form request details for the shipment. |
| `id` | path | `string` | yes | EasyPost Shipment ID, beginning with shp_. |
