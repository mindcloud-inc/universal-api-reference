# Reset Password Token with Cryptolens

Creates a password reset token in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/userauth/ResetPasswordToken`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Reset Password Token](https://app.cryptolens.io/docs/api/v3/ResetPasswordToken)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Username` | query | `string` | yes | The username. |
