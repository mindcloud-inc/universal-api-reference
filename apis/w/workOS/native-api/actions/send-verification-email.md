# Send verification email with WorkOS

Sends a verification email in your WorkOS environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/user_management/users/{id}/email_verification/send`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [Send verification email](https://workos.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the user. |
