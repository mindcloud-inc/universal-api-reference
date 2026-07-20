# Call Device Function with Particle

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/devices/:deviceId/:functionName`
- **Base URL:** `https://api.particle.io`
- **Official documentation:** [Call Device Function](https://docs.particle.io/reference/cloud-apis/api/#call-a-function)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `arg` | body | `string` | yes |
| `deviceId` | path | `string` | yes |
| `functionName` | path | `string` | yes |
