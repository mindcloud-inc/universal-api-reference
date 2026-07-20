# Send OTP with Tellephant

Sends an OTP message through Tellephant.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/send-otp`
- **Base URL:** `https://api.tellephant.com`
- **Official documentation:** [Send OTP](https://app.tellephant.com/api-documentation#otp-service)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `number` | yes | Recipient phone number with country code. |
| `organisation_name` | body | `string` | yes | Organization name shown in the OTP message. |
