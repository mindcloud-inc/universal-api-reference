# Download the specified recording with Digital Samba

Retrieves a recording download from Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/recordings/:recording/download`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Download the specified recording](https://developer.digitalsamba.com/rest-api/#recordings-GETapi-v1-recordings--recording--download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recording` | path | `string` | yes | Recording path parameter. |
| `valid_for_minutes` | query | `number` | no | Link expiration time in minutes. |
