# Send OTP with D7 Messaging

Sends a one-time password through D7 Messaging.

## Endpoint

- **Method:** `POST`
- **Path:** `/verify/v1/otp/send-otp`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Send OTP](https://d7networks.com/docs/verify/send-otp/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipient` | body | `string` | yes | Recipient phone number in E.164 format including country code. |
| `content` | body | `string` | no | OTP message content. Use {} where the OTP code should be inserted. |
| `template_id` | body | `number` | no | Dashboard template ID to use instead of Content. |
| `originator` | body | `string` | no | Sender name shown to the recipient. |
| `channel` | body | `string` | no | Channel used to deliver the OTP, such as SMS or WhatsApp. |
| `expiry` | body | `number` | no | OTP validity period in seconds. |
| `data_coding` | body | `string` | no | Encoding mode for the OTP content: text, unicode, or auto. |
