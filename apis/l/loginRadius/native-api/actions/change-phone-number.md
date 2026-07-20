# Change Phone Number with LoginRadius

Updates a phone number in LoginRadius.

## Endpoint

- **Method:** `PUT`
- **Path:** `/identity/v2/auth/phone`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Change Phone Number](https://www.loginradius.com/docs/api/openapi/change-phone-number/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_token` | query | `string` | yes | Access Token of the user. |
| `phone` | body | `string` | yes | New phone number. |
