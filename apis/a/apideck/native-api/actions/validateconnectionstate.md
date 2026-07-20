# Validate Connection State with Apideck

Validates a connection state in Apideck Vault.

## Endpoint

- **Method:** `POST`
- **Path:** `/vault/connections/:unified_api/:service_id/validate`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Validate Connection State](https://developers.apideck.com/apis/vault/reference/connections)

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
