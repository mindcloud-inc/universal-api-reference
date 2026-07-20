# Delete custom mapping with Apideck

Deletes an existing custom mapping from Apideck Vault.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/vault/custom-mappings/:unified_api/:service_id/:target_field_id`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Delete custom mapping](https://developers.apideck.com/apis/vault/reference/custom-mappings)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `unified_api` | path | `string` | yes |
| `service_id` | path | `string` | yes |
| `target_field_id` | path | `string` | yes |
