# Get OTP Status with SMS Connexion

Retrieves an OTP status from SMS Connexion.

## Endpoint

- **Method:** `GET`
- **Path:** `/otp/:otpId`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Get OTP Status](https://sms.cx/sms-api-documentation/#operation/GetOtpStatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `otpId` | path | `string` | yes | OTP UUID returned by Create OTP. |
