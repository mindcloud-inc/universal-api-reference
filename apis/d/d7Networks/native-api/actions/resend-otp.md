# Resend OTP with D7 Networks

Resends a one-time password with D7 Networks.

## Endpoint

- **Method:** `POST`
- **Path:** `/verify/v1/otp/resend-otp`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Resend OTP](https://d7networks.com/docs/verify/resend-otp/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `otp_id` | body | `string` | yes | OTP ID returned by Send OTP. |
