# MFA Login with LoginRadius

Creates a LoginRadius access token with MFA.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/v2/auth/login/2fa`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [MFA Login](https://www.loginradius.com/docs/api/openapi/mfa-login/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | yes | Email address used for MFA login. |
| `Password` | body | `string` | yes | Password used for MFA login. |
