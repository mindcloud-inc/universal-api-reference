# Validate OTP with Tellephant

Validates an OTP code in Tellephant.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/validate-otp`
- **Base URL:** `https://api.tellephant.com`
- **Official documentation:** [Validate OTP](https://app.tellephant.com/api-documentation#otp-service)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `otpId` | body | `string` | yes | OTP ID returned by Send OTP. |
| `otp` | body | `number` | yes | One-time passcode entered by the user. |
