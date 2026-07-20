# List statistics versions with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/statistics/versions`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List statistics versions](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id[]` | query | `array<number>` | no | ID of product |
| `type[]` | query | `array<string>` | no | Statistic type |
| `version[]` | query | `array<string>` | no | Version of firmware |
