# Create OTP with SMS Connexion

Creates a new OTP in SMS Connexion.

## Endpoint

- **Method:** `POST`
- **Path:** `/otp`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Create OTP](https://sms.cx/sms-api-documentation/#operation/NewOtp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumber` | body | `string` | yes | Recipient phone number in E.164 format. |
