# Get Device Status with Airzone Cloud

Retrieves a device's state from Airzone Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/devices/{deviceId}/status`
- **Base URL:** `https://m.airzonecloud.com/api/v1`
- **Official documentation:** [Get Device Status](https://developers.airzonecloud.com/docs/web-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceId` | path | `string` | yes | The Airzone device identifier. |
| `installation_id` | query | `string` | yes | The installation ID that owns the device. |
