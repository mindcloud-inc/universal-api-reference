# Get User by Refresh Token with Instant

Retrieves a user from Instant by refresh token.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/users`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Get User by Refresh Token](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refresh_token` | query | `string` | yes | Refresh token to look up. |
