# List Materials with DateX (Legacy)

## Endpoint

- **Method:** `POST`
- **Path:** `materials/get`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [List Materials](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_materials_get)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | — |
| `filters.owner[]` | body | `array<string>` | no | — |
| `filters.project[]` | body | `array<string>` | no | — |
| `filters.status[]` | body | `array<string>` | no | — |
| `filters.lookup[]` | body | `array<string>` | no | An Array of lookup fields |
| `filters.global_material_name[]` | body | `array<string>` | no | — |
| `filters.materialName[]` | body | `array<string>` | no | — |
| `filters.materialGroup[]` | body | `array<string>` | no | — |
| `filters.material_id[]` | body | `array<number>` | no | — |
| `filters.upc[]` | body | `array<string>` | no | — |
