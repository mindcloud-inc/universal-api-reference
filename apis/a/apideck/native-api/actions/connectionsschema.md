# Get resource schema with Apideck

Retrieves a resource schema from Apideck Vault.

## Endpoint

- **Method:** `GET`
- **Path:** `/vault/connections/:unified_api/:service_id/:resource/schema`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Get resource schema](https://developers.apideck.com/apis/vault/reference/connections)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `unified_api` | path | `string` | yes |
| `service_id` | path | `string` | yes |
| `resource` | path | `string` | yes |
