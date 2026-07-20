# Create Webhook with Particle

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/integrations`
- **Base URL:** `https://api.particle.io`
- **Official documentation:** [Create Webhook](https://docs.particle.io/reference/cloud-apis/api/#create-a-webhook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event` | body | `string` | yes |
| `integration_type` | body | `string` | yes |
| `name` | body | `string` | no |
| `requestType` | body | `string` | yes |
| `url` | body | `string` | yes |
