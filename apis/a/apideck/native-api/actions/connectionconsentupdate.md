# Update consent state with Apideck

Updates a connection consent state in Apideck Vault.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/vault/connections/:unified_api/:service_id/consent`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Update consent state](https://developers.apideck.com/apis/vault/reference/connections)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `service_id` | path | `string` | yes |
| `unified_api` | path | `string` | yes |
| `resources` | body | `object` | yes |
| `granted` | body | `boolean` | yes |
