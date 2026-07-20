# Change Password with Cryptolens

Updates a user password in Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/userauth/ChangePassword`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Change Password](https://app.cryptolens.io/docs/api/v3/ChangePassword)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Username` | query | `string` | yes | The username. |
| `NewPassword` | query | `string` | yes | The new password. |
