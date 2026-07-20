# Verify OTP with SMS Connexion

Verifies an OTP in SMS Connexion.

## Endpoint

- **Method:** `POST`
- **Path:** `/otp/:otpId`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Verify OTP](https://sms.cx/sms-api-documentation/#operation/VerifyPin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `otpId` | path | `string` | yes | OTP UUID returned by Create OTP. |
| `pin` | body | `string` | yes | OTP PIN code to verify. |
