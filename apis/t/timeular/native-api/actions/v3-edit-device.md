# V3 Edit Device with Timeular

Updates an existing device in the Timeular v3 API.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/devices/:deviceId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V3 Edit Device](https://developers.early.app/#78ab7505-587f-469a-974f-781647bc4900)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `deviceId` | path | `string` | yes |
| `name` | body | `string` | no |
