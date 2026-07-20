# Verify OTP with D7 Networks

Verifies a one-time password with D7 Networks.

## Endpoint

- **Method:** `POST`
- **Path:** `/verify/v1/otp/verify-otp`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Verify OTP](https://d7networks.com/docs/verify/verify-otp/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `otp_id` | body | `string` | yes | OTP ID returned by Send OTP. |
| `otp_code` | body | `string` | yes | OTP code received by the recipient. |
