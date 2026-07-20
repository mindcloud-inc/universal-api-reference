# Create Refresh Token by Email with Instant

Creates a refresh token in Instant by email.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/refresh_tokens`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Create Refresh Token by Email](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | User email address to issue a refresh token for. |
