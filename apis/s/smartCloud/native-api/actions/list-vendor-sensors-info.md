# List sensors info with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/vendor/sensors-info`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List sensors info](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_version_id` | query | `number` | no | ID of product version |
| `language` | query | `string` | no | Language of info |
| `sensor` | query | `string` | no | Topic of sensor |
| `search` | query | `string` | no | Search for entity |
