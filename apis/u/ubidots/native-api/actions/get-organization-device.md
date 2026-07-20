# Get Organization Device with Ubidots

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_key/devices/:device_key/`
- **Base URL:** `https://industrial.api.ubidots.com/api/v2.0`
- **Official documentation:** [Get Organization Device](https://docs.ubidots.com/reference/get-device-in-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_key` | path | `string` | yes | The organization ID or key. |
| `device_key` | path | `string` | yes | The device ID or API label. |
