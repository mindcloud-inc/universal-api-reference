# Test Integration with Particle

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/integrations/:integrationId/test`
- **Base URL:** `https://api.particle.io`
- **Official documentation:** [Test Integration](https://docs.particle.io/reference/cloud-apis/api/#test-an-integration)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data` | body | `string` | no |
| `device_id` | body | `string` | no |
| `integrationId` | path | `string` | yes |
