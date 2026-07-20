# Authorize Access Token with Apideck

Authorizes stored connection credentials in Apideck Vault.

## Endpoint

- **Method:** `POST`
- **Path:** `/vault/connections/:unified_api/:service_id/token`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Authorize Access Token](https://developers.apideck.com/apis/vault/reference/connections)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `service_id` | path | `string` | yes |
| `unified_api` | path | `string` | yes |
