# Check 2FA Code with Nvoip

## Endpoint

- **Method:** `GET`
- **Path:** `/check/2fa`
- **Base URL:** `https://api.nvoip.com.br/v2`
- **Official documentation:** [Check 2FA Code](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/2fa.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pin` | query | `string` | yes | Verification PIN received by the user. |
| `token2fa` | query | `string` | yes | Token returned by the Send 2FA Code action. |
