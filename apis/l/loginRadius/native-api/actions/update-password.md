# Update Password with LoginRadius

Updates an existing password in LoginRadius.

## Endpoint

- **Method:** `PUT`
- **Path:** `/identity/v2/auth/password/change`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Update Password](https://www.loginradius.com/docs/api/openapi/change-password/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_token` | query | `string` | yes | Access Token of the user. |
| `OldPassword` | body | `string` | yes | Current password for verification. |
| `NewPassword` | body | `string` | yes | New password to set. |
