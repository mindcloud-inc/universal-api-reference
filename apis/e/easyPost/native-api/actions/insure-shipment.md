# Insure Shipment with EasyPost

Creates shipping insurance for a shipment in EasyPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipments/:id/insure`
- **Base URL:** `https://api.easypost.com/v2`
- **Official documentation:** [Insure Shipment](https://docs.easypost.com/docs/shipments/shipping-insurance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `string` | yes | Insurance amount to add to the shipment. |
| `id` | path | `string` | yes | EasyPost Shipment ID, beginning with shp_. |
