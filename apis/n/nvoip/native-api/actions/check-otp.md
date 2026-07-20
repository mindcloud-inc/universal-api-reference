# Check OTP with Nvoip

## Endpoint

- **Method:** `GET`
- **Path:** `/check/otp`
- **Base URL:** `https://api.nvoip.com.br/v2`
- **Official documentation:** [Check OTP](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/otp.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | query | `string` | yes | OTP code received by the user. |
| `key` | query | `string` | yes | OTP key returned by the Send OTP action. |
