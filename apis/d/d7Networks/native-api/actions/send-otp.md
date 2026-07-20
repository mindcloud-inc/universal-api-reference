# Send OTP with D7 Networks

Sends a one-time password with D7 Networks.

## Endpoint

- **Method:** `POST`
- **Path:** `/verify/v1/otp/send-otp`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Send OTP](https://d7networks.com/docs/verify/send-otp/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipient` | body | `string` | yes | Recipient phone number with country code. |
| `originator` | body | `string` | no | Sender ID or brand name. |
| `content` | body | `string` | yes | OTP message content; include {} as the OTP placeholder. |
| `expiry` | body | `number` | no | OTP expiry in seconds. |
| `channel` | body | `string` | no | OTP delivery channel. Defaults to SMS. |
| `data_coding` | body | `string` | no | Text encoding; text, unicode, or auto. |
