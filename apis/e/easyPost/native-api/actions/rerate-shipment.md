# Rerate Shipment with EasyPost

Refreshes rates for an existing shipment in EasyPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipments/:id/rerate`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Rerate Shipment](https://docs.easypost.com/docs/shipments/rates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EasyPost Shipment ID, beginning with shp_. |
