# List Shipping Details with DateX (Legacy)

## Endpoint

- **Method:** `POST`
- **Path:** `shipments/shipping_details/get`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [List Shipping Details](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_shipments_shipping_details_get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `exclude.user_defined_fields` | body | `boolean` | no |
| `filters` | body | `object` | no |
| `filters.order_ids[]` | body | `array<number>` | no |
| `exclude` | body | `object` | no |
| `filters.order_lookups[]` | body | `array<string>` | no |
| `filters.shipment_ids[]` | body | `array<number>` | no |
| `filters.shipment_lookups[]` | body | `array<string>` | no |
