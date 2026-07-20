# Update firmware with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/firmwares/{id}/ap/update`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Update firmware](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of entity |
| `ssid` | body | `string` | no | Ap ssid |
| `password` | body | `string` | no | Ap password |
