# Update consumer with Apideck

Updates an existing consumer in Apideck Vault.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/vault/consumers/:consumer_id`
- **Base URL:** `https://unify.apideck.com`
- **Official documentation:** [Update consumer](https://developers.apideck.com/apis/vault/reference/consumers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `consumer_id` | path | `string` | yes |
| `metadata` | body | `object` | no |
