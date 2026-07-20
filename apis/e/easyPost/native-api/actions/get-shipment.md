# Get Shipment with EasyPost

Retrieves details for a shipment from EasyPost.

## Endpoint

- **Method:** `GET`
- **Path:** `/shipments/:id`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Get Shipment](https://docs.easypost.com/docs/shipments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EasyPost Shipment ID, beginning with shp_. |
