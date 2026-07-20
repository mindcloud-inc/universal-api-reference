# Delete firmware build with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/firmware-builds/{id}/delete`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Delete firmware build](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of entity |
| `product_version_id` | body | `number` | yes | ID of product version |
