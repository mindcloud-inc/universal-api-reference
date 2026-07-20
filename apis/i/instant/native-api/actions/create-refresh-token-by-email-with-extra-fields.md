# Create Refresh Token by Email With Extra Fields with Instant

Creates a refresh token in Instant by email, setting extra fields on user creation.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/refresh_tokens`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Create Refresh Token by Email With Extra Fields](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | User email address to issue a refresh token for. |
| `extra-fields` | body | `object` | no | Optional custom $users fields to set when creating the user. |
