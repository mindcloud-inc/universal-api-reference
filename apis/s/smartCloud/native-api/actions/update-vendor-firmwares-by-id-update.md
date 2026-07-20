# Update firmware with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/firmwares/{id}/update`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Update firmware](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of entity |
| `title` | body | `string` | no | Firmware title |
| `firmware_base` | body | `string` | no | Firmware base |
| `config` | body | `string` | no | Firmware config |
