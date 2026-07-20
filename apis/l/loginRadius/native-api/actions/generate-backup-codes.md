# Generate Backup Codes with LoginRadius

Retrieves MFA backup codes from LoginRadius.

## Endpoint

- **Method:** `GET`
- **Path:** `/identity/v2/auth/account/2fa/backupcode`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Generate Backup Codes](https://www.loginradius.com/docs/api/openapi/mfa-generate-backup-codes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_token` | query | `string` | yes | Access Token of the user. |
