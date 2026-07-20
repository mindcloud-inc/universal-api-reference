# Authorize with Apideck

Starts an OAuth authorization flow in Apideck Vault.

## Endpoint

- **Method:** `GET`
- **Path:** `/vault/authorize/:service_id/:application_id`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Authorize](https://developers.apideck.com/apis/vault/reference/connections)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `service_id` | path | `string` | yes |
| `state` | query | `string` | yes |
| `redirect_uri` | query | `string` | yes |
| `scope` | query | `list<string>` | no |
