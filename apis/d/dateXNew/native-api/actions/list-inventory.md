# List Inventory with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `inventory/get`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [List Inventory](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_inventory_get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `warehouse` | body | `string` | yes | Warehouse lookup/name to query inventory for. |
| `filters.project` | body | `string` | yes | Project filter. Required by the DateX API. |
| `filters.owner` | body | `string` | no | Owner filter. |
| `filters.material` | body | `string` | no | Material filter. |
| `filters.lot` | body | `string` | no | Lot filter. |
| `filters.vendor_lot` | body | `string` | no | Vendor lot filter. |
| `filters.upc` | body | `string` | no | UPC filter. |
| `output_weight_uom` | body | `string` | no | Optional output weight unit of measure. |
