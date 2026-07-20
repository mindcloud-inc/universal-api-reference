# List Available Inventory with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `inventory_availability/get`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [List Available Inventory](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_inventory_availability_get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `warehouse` | body | `string` | yes | Warehouse lookup/name to query inventory availability for. |
| `filters.project` | body | `string` | yes | Project filter. Required by the DateX API. |
| `filters.owner` | body | `string` | no | Owner filter. |
| `filters.material` | body | `string` | no | Material filter. |
| `filters.upc` | body | `string` | no | UPC filter. |
