# Login With Credentials with LoginRadius

Creates a LoginRadius access token from user credentials.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/v2/auth/login`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Login With Credentials](https://www.loginradius.com/docs/api/openapi/email-by-login-user-name-phone/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | yes | Email, username, or phone identifier to log in with. |
| `Password` | body | `string` | yes | Password for the account. |
