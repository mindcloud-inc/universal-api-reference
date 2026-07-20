# Buy Shipment with EasyPost

Purchases an existing shipment in EasyPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipments/:id/buy`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Buy Shipment](https://docs.easypost.com/docs/shipments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EasyPost Shipment ID, beginning with shp_. |
| `rate` | body | `object` | yes | Selected EasyPost rate object or rate ID payload for buying the shipment. |
