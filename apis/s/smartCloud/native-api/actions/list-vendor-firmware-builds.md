# List firware builds with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/firmware-builds`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List firware builds](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | no | ID of entity |
| `status[]` | query | `array<string>` | no | Firmware build status |
| `type` | query | `string` | no | Firmware build type |
| `firmware_id[]` | query | `array<number>` | no | ID of firmware |
| `firmware_id[]` | query | `array<number>` | no | ID of firmware |
| `product_id[]` | query | `array<number>` | no | ID of firmware |
| `product_id[]` | query | `array<number>` | no | ID of firmware |
| `sort` | query | `string` | no | Sort key |
| `order` | query | `string` | no | Sort order |
| `updated_from` | query | `string` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `updated_to` | query | `string` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_from` | query | `string` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_to` | query | `string` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `limit` | query | `number` | no | The number of rows to return |
| `offset` | query | `number` | no | Pagination offset |
