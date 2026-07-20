# Create API Key with jo4.io

## Endpoint

- **Method:** `POST`
- **Path:** `/protected/api-keys`
- **Base URL:** `https://jo4-api.jo4.io/api/v1`
- **Official documentation:** [Create API Key](https://jo4-api.jo4.io/swagger-ui/index.html#/api-key-controller/createApiKey)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `expiresAt` | body | `number` | no |
| `name` | body | `string` | yes |
| `scopes` | body | `string` | no |
