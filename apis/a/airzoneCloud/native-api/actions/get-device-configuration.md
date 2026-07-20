# Get Device Configuration with Airzone Cloud

Retrieves device configuration from Airzone Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/devices/{deviceId}/config`
- **Base URL:** `https://m.airzonecloud.com/api/v1`
- **Official documentation:** [Get Device Configuration](https://developers.airzonecloud.com/docs/web-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceId` | path | `string` | yes | The Airzone device identifier. |
| `installation_id` | query | `string` | yes | The installation ID that owns the device. |
| `type` | query | `string` | yes | Required Airzone configuration scope. Supported values are `all`, `user`, and `advanced`. |
