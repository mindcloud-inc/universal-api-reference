# Get Device Last Values with Ubidots

## Endpoint

- **Method:** `GET`
- **Path:** `/devices/:device_key/_/values/last`
- **Base URL:** `https://industrial.api.ubidots.com/api/v2.0`
- **Official documentation:** [Get Device Last Values](https://docs.ubidots.com/reference/get-device-last-values)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_key` | path | `string` | yes | The device ID or API label. |
