# Resend OTP with D7 Messaging

Resends a one-time password through D7 Messaging.

## Endpoint

- **Method:** `POST`
- **Path:** `/verify/v1/otp/resend-otp`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Resend OTP](https://d7networks.com/docs/verify/resend-otp/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `otp_id` | body | `string` | yes | OTP ID returned by Send OTP. |
