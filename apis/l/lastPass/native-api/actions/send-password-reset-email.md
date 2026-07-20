# Send Password Reset Email with LastPass

Sends a password reset email to a LastPass user.

## Endpoint

- **Method:** `POST`
- **Path:** `/enterpriseapi.php`
- **Base URL:** `https://lastpass.com`
- **Official documentation:** [Send Password Reset Email](https://support.lastpass.com/help/lastpass-provisioning-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address of the user who should receive a password reset email. |
