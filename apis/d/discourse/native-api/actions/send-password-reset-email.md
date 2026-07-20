# Send Password Reset Email with Discourse

Sends a Discourse password reset email.

## Endpoint

- **Method:** `POST`
- **Path:** `/session/forgot_password.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Send Password Reset Email](https://docs.discourse.org/#tag/Users/operation/sendPasswordResetEmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `login` | body | `string` | yes | Username or email address to send the password reset email to. |
