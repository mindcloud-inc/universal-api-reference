# Update Application Token with EMnify

Updates an existing application token in EMnify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/application_token/:application_token_id`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [Update Application Token](https://docs.emnify.com/developers/api/application-tokens/application-token-by-id-patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `application_token_id` | path | `number` | yes | Application token ID to update. |
| `description` | body | `string` | no | Updated token description. |
| `expiry_date` | body | `string` | no | Updated expiry date. |
| `ip` | body | `string` | no | Updated IP/CIDR restriction. |
