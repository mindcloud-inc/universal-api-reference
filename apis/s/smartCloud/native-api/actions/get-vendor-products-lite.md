# List products with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/products/lite`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List products](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id[]` | query | `array<number>` | no | IDs of entities |
| `limit` | query | `number` | no | The number of rows to return |
| `offset` | query | `number` | no | Pagination offset |
| `is_archived` | query | `boolean` | no | Is this entity archived |
