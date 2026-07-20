# Resend Verification Email with LoginRadius

Resends an email verification message from LoginRadius.

## Endpoint

- **Method:** `PUT`
- **Path:** `/identity/v2/auth/register`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Resend Verification Email](https://www.loginradius.com/docs/api/openapi/resend-email-verification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to resend the verification email to. |
