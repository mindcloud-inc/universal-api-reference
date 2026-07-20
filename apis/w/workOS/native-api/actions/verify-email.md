# Verify email with WorkOS

Verifies an email in your WorkOS environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/user_management/users/{id}/email_verification/confirm`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Verify email](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the user. |
| `code` | body | `string` | yes | The one-time email verification code. |
