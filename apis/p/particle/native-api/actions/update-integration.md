# Update Integration with Particle

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/integrations/:integrationId`
- **Base URL:** `https://api.particle.io`
- **Official documentation:** [Update Integration](https://docs.particle.io/reference/cloud-apis/api/#edit-a-webhook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event` | body | `string` | yes |
| `integration_type` | body | `string` | yes |
| `integrationId` | path | `string` | yes |
| `name` | body | `string` | no |
| `requestType` | body | `string` | yes |
| `url` | body | `string` | yes |
