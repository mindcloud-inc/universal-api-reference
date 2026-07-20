# Create firmware changelog with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/firmware-changelogs`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Create firmware changelog](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of firmware |
| `changelog` | body | `string` | no | Changelog text of firmware |
| `product_version_id` | body | `number` | yes | ID of product version |
