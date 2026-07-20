# Verify Email with LoginRadius

Verifies an email address in LoginRadius.

## Endpoint

- **Method:** `PUT`
- **Path:** `/identity/v2/auth/email`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Verify Email](https://www.loginradius.com/docs/api/openapi/update-email/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address being verified. |
| `otp` | body | `string` | no | Email verification OTP. |
| `verificationtoken` | body | `string` | no | Email verification token. |
