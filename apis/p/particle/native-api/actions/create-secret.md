# Create Secret with Particle

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/secrets`
- **Base URL:** `https://api.particle.io`
- **Official documentation:** [Create Secret](https://docs.particle.io/reference/cloud-apis/api/#create-a-cloud-secret)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `secret.name` | body | `string` | yes |
| `secret.value` | body | `string` | yes |
