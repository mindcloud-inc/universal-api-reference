# Retrieve MFA Settings with LoginRadius

Retrieves MFA account settings from LoginRadius.

## Endpoint

- **Method:** `GET`
- **Path:** `/identity/v2/auth/account/2fa`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Retrieve MFA Settings](https://www.loginradius.com/docs/api/openapi/get-mfa-settings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_token` | query | `string` | yes | Access Token of the user. |
| `duoredirecturi` | query | `string` | no | Duo auth redirection URL. |
