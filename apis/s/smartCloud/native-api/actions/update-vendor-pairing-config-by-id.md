# Update pairing config with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/pairing-config/{id}`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Update pairing config](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of entity |
| `config` | body | `string` | no | Config JSON string |
