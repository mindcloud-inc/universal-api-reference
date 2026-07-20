# Approve products with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/products/approve`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Approve products](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id[]` | query | `array<number>` | no | IDs of entities |
| `type` | query | `string` | no | Type of product |
| `abbreviation` | query | `number` | no | Abbreviation of product |
