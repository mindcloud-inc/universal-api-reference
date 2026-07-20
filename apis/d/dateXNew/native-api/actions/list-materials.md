# List Materials with DateX

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
| `filters.project[]` | body | `array<string>` | yes | Project filters. Required by the DateX API. |
| `filters.owner[]` | body | `array<string>` | no | Owner filters. |
| `filters.lookup[]` | body | `array<string>` | no | Material lookup filters. |
| `filters.status[]` | body | `array<string>` | no | Material status filters. |
| `filters.global_material_name[]` | body | `array<string>` | no | Global material name filters. |
| `filters.material_name[]` | body | `array<string>` | no | Material name filters. |
| `filters.material_group[]` | body | `array<string>` | no | Material group filters. |
| `filters.material_id[]` | body | `array<number>` | no | Material ID filters. |
