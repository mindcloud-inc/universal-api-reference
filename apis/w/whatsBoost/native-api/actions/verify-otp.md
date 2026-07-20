# Verify OTP with WhatsBoost

Verifies a one-time password in WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/get/otp`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Verify OTP](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `otp` | body | `string` | yes | The otp you got from a user supplied input or data |
