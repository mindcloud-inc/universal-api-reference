# Create Refresh Token by User ID with Instant

Creates a refresh token in Instant by user ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/refresh_tokens`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Create Refresh Token by User ID](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Instant user ID to issue a refresh token for. |
