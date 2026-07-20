# List Warehouses with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `warehouses/get`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [List Warehouses](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_warehouses_get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters.names[]` | body | `array<string>` | no | Warehouse name filters. |
