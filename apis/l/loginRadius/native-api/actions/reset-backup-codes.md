# Reset Backup Codes with LoginRadius

Resets MFA backup codes in LoginRadius.

## Endpoint

- **Method:** `GET`
- **Path:** `/identity/v2/auth/account/2fa/backupcode/reset`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Reset Backup Codes](https://www.loginradius.com/docs/api/openapi/mfa-reset-backup-codes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_token` | query | `string` | yes | Access Token of the user. |
