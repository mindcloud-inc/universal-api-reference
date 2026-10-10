# Update Webhook with PestPac

## Endpoint

- **Method:** `PUT`
- **Path:** `WebHooks/:id`
- **Base URL:** `https://api.workwave.com/pestpac/v1/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `EntityType` | body | `string` | no |
| `postToUrl` | body | `string` | no |
| `action` | body | `string` | no |
| `includeEntityBody` | body | `boolean` | no |
| `id` | path | `string` | no |
