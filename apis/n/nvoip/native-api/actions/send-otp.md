# Send OTP with Nvoip

## Endpoint

- **Method:** `POST`
- **Path:** `/otp`
- **Base URL:** `https://api.nvoip.com.br/v2`
- **Official documentation:** [Send OTP](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/otp.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Email address that should receive the OTP. |
| `sms` | body | `string` | no | Phone number that should receive the OTP by SMS. |
| `voice` | body | `string` | no | Phone number that should receive the OTP by voice. |
| `methods.email` | body | `boolean` | no | Whether to deliver the OTP by email. |
| `methods.sms` | body | `boolean` | no | Whether to deliver the OTP by SMS. |
| `methods.voice` | body | `boolean` | no | Whether to deliver the OTP by voice call. |
