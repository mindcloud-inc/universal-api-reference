# Revoke connection with Apideck

Starts a connection revoke flow in Apideck Vault.

## Endpoint

- **Method:** `GET`
- **Path:** `/vault/revoke/:service_id/:application_id`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Revoke connection](https://developers.apideck.com/apis/vault/reference/connections)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `service_id` | path | `string` | yes |
| `state` | query | `string` | yes |
| `redirect_uri` | query | `string` | yes |
