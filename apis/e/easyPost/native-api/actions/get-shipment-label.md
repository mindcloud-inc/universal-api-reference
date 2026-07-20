# Get Shipment Label with EasyPost

Retrieves a label for a shipment from EasyPost.

## Endpoint

- **Method:** `GET`
- **Path:** `/shipments/:id/label`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Get Shipment Label](https://docs.easypost.com/docs/shipments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EasyPost Shipment ID, beginning with shp_. |
