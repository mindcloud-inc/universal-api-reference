# Update Materials with DateX (Legacy)

## Endpoint

- **Method:** `POST`
- **Path:** `materials/update`
- **Base URL:** `https://{environment}.wavelength.host/api/`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `materials[]` | body | `array` | no | — |
| `materials[].packagings[]` | body | `array` | no | — |
| `materials[].packagings[].packaging` | body | `string` | no | Eg: "EA" |
| `materials[].material_id` | body | `number` | no | — |
| `materials[].packagings[].length` | body | `number` | no | — |
| `materials[].packagings[].width` | body | `number` | no | — |
| `materials[].packagings[].height` | body | `number` | no | — |
| `materials[].packagings[].dimension_uom` | body | `string` | no | Eg: "ft" |
| `materials[].packagings[].net_weight` | body | `number` | no | Eg: 'kg', 'lb' |
| `materials[].packagings[].gross_weight` | body | `number` | no | — |
| `materials[].packagings[].weight_uom` | body | `string` | no | eg: 'kg', 'lb' |
| `materials[].packagings[].net_volume` | body | `number` | no | — |
| `materials[].packagings[].volume_uom` | body | `string` | no | eg: 'cu. ft.' |
| `materials[].packagings[].gross_volume` | body | `number` | no | — |
