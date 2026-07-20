# Rename Device with Particle

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/devices/:deviceId`
- **Base URL:** `https://api.particle.io`
- **Official documentation:** [Rename Device](https://docs.particle.io/reference/cloud-apis/api/#rename-a-device)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `deviceId` | path | `string` | yes |
| `name` | body | `string` | yes |
