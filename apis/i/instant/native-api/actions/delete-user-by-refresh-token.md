# Delete User by Refresh Token with Instant

Deletes a user from Instant by refresh token.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/admin/users`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Delete User by Refresh Token](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refresh_token` | query | `string` | yes | Refresh token whose user should be deleted. |
