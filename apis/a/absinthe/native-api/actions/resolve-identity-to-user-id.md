# Resolve Identity to User ID with Absinthe

Finds a user ID in Absinthe by identity.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/resolve`
- **Base URL:** `https://api.absinthe.network`
- **Official documentation:** [Resolve Identity to User ID](https://api.absinthe.network/doc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `identity_type` | query | `string` | yes |
| `identity_value` | query | `string` | yes |
