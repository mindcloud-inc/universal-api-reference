# Create Callback State with Apideck

Creates a callback state in Apideck Vault.

## Endpoint

- **Method:** `POST`
- **Path:** `/vault/connections/:unified_api/:service_id/callback-state`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Create Callback State](https://developers.apideck.com/apis/vault/reference/connections)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `service_id` | path | `string` | yes |
| `unified_api` | path | `string` | yes |
| `redirect_uri` | body | `string` | yes |
