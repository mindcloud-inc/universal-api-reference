# List statistics intervals with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/statistics/version-intervals`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List statistics intervals](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id[]` | query | `array<number>` | no | ID of product |
| `type[]` | query | `array<string>` | no | Statistic type |
| `interval` | query | `string` | no | Statistic interval (long) |
| `version[]` | query | `array<string>` | no | Version of firmware |
| `created_from` | query | `string` | no | Starting from datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
| `created_to` | query | `string` | no | Till datetime YYYY-MM-DDTHH:MM:SSZ (RFC3339) |
