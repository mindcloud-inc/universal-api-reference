# List Inventory with DateX (Legacy)

## Endpoint

- **Method:** `POST`
- **Path:** `inventory/get`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [List Inventory](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_inventory_get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters.owner` | body | `string` | no |
| `warehouse` | body | `string` | yes |
| `filters` | body | `object<object>` | no |
| `filters.project` | body | `string` | yes |
| `filters.material` | body | `string` | no |
| `output_weight_uom` | body | `string` | no |
| `filters.lot` | body | `string` | no |
| `filters.vendor_lot` | body | `string` | no |
| `filters.upc` | body | `string` | no |
