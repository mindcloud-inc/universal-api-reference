# Create firmware with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/firmwares`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Create firmware](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Firmware title |
| `firmware_base` | body | `string` | yes | Firmware base |
| `config` | body | `string` | no | Firmware config |
