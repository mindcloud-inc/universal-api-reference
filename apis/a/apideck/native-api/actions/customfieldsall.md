# Get resource custom fields with Apideck

Retrieves resource custom fields from Apideck Vault.

## Endpoint

- **Method:** `GET`
- **Path:** `/vault/connections/:unified_api/:service_id/:resource/custom-fields`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Get resource custom fields](https://developers.apideck.com/apis/vault/reference/connections)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `unified_api` | path | `string` | yes |
| `service_id` | path | `string` | yes |
| `resource` | path | `string` | yes |
| `resource_id` | query | `string` | no |
