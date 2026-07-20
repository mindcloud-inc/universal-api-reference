# Cancel OTP with SMS Connexion

Deletes an existing OTP from SMS Connexion.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/otp/:otpId`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Cancel OTP](https://sms.cx/sms-api-documentation/#operation/CancelOtp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `otpId` | path | `string` | yes | OTP UUID returned by Create OTP. |
