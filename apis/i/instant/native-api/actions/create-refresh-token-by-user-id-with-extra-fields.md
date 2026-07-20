# Create Refresh Token by User ID With Extra Fields with Instant

Creates a refresh token in Instant by ID, setting extra fields on creation.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/refresh_tokens`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Create Refresh Token by User ID With Extra Fields](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Instant user ID to issue a refresh token for. |
| `extra-fields` | body | `object` | no | Optional custom $users fields to set when creating the user. |
