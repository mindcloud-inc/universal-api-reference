# Sensor info update with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/sensors-info/update`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Sensor info update](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_version_id` | body | `number` | no | Product version id |
| `sensor` | body | `string` | no | Sensor topic |
| `info` | body | `object` | no | — |
