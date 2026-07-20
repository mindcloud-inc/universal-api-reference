# Create a password reset token with WorkOS

Creates a password reset token in your WorkOS environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/user_management/password_reset`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Create a password reset token](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address of the user requesting a password reset. |
