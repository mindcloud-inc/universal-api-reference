# List connection custom mappings with Apideck

Retrieves connection custom mappings from Apideck Vault.

## Endpoint

- **Method:** `GET`
- **Path:** `/vault/connections/:unified_api/:service_id/:resource/custom-mappings`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [List connection custom mappings](https://developers.apideck.com/apis/vault/reference/connections)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `unified_api` | path | `string` | yes |
| `service_id` | path | `string` | yes |
| `resource` | path | `string` | yes |
| `resource_id` | query | `string` | no |
