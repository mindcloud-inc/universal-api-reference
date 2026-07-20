# List devices with 2Smart Cloud

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/devices`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [List devices](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id[]` | query | `array<number>` | no | IDs of entities |
| `status[]` | query | `array<string>` | no | Device connection status |
| `user_email` | query | `string` | no | Email of device owner |
| `sort` | query | `string` | no | Sort key |
| `limit` | query | `number` | no | The number of rows to return |
| `offset` | query | `number` | no | Pagination offset |
