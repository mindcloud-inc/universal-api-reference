# Update Secret with Particle

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/secrets/:secretName`
- **Base URL:** `https://api.particle.io`
- **Official documentation:** [Update Secret](https://docs.particle.io/reference/cloud-apis/api/#create-or-update-the-value-of-a-cloud-secret)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `secret.value` | body | `string` | yes |
| `secretName` | path | `string` | yes |
