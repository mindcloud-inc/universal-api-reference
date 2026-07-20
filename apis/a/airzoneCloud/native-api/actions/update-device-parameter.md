# Update Device Parameter with Airzone Cloud

Updates a device parameter in Airzone Cloud.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/devices/{deviceId}`
- **Base URL:** `https://m.airzonecloud.com/api/v1`
- **Official documentation:** [Update Device Parameter](https://developers.airzonecloud.com/docs/web-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceId` | path | `string` | yes | The Airzone device identifier. |
| `installation_id` | body | `string` | yes | The installation ID that owns the device. |
| `opts` | body | `object` | no | Optional object for extra settings, such as `units` when updating a setpoint. |
| `param` | body | `string` | yes | The device parameter to change. |
| `value` | body | `string` | yes | The new parameter value. |
