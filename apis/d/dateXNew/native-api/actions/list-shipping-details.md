# List Shipping Details with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `shipments/shipping_details/get`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [List Shipping Details](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_shipments_shipping_details_get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters.order_ids[]` | body | `array<number>` | no | Order ID filters. |
| `filters.order_lookups[]` | body | `array<string>` | no | Order lookup filters. |
| `filters.shipment_ids[]` | body | `array<number>` | no | Shipment ID filters. |
| `filters.shipment_lookups[]` | body | `array<string>` | no | Shipment lookup filters. |
