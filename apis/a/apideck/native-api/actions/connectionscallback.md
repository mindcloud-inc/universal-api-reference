# Callback with Apideck

Handles an OAuth callback in Apideck Vault.

## Endpoint

- **Method:** `GET`
- **Path:** `/vault/callback`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Callback](https://developers.apideck.com/apis/vault/reference/connections)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `state` | query | `string` | yes |
| `code` | query | `string` | yes |
| `error` | query | `string` | no |
| `error_description` | query | `string` | no |
