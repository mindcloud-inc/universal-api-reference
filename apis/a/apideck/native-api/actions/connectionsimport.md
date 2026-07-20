# Import connection with Apideck

Imports an authorized connection into Apideck Vault.

## Endpoint

- **Method:** `POST`
- **Path:** `/vault/connections/:unified_api/:service_id/import`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Import connection](https://developers.apideck.com/apis/vault/reference/connections)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `service_id` | path | `string` | yes |
| `unified_api` | path | `string` | yes |
| `credentials` | body | `object` | no |
| `settings` | body | `object` | no |
| `metadata` | body | `object` | no |
