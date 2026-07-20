# Consumer request counts with Apideck

Retrieves consumer request counts from Apideck Vault.

## Endpoint

- **Method:** `GET`
- **Path:** `/vault/consumers/:consumer_id/stats`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Consumer request counts](https://developers.apideck.com/apis/vault/reference/consumers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `consumer_id` | path | `string` | yes |
| `start_datetime` | query | `string` | yes |
| `end_datetime` | query | `string` | yes |
