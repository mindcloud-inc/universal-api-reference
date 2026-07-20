# Forgot Password with LoginRadius

Sends a password reset request in LoginRadius.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/v2/auth/password`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Forgot Password](https://www.loginradius.com/docs/api/openapi/forgot-password/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | yes | Email address for password recovery. |
| `UserName` | body | `string` | no | User name for password recovery. |
