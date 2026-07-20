# Send Telegram OTP with Messaggio

Creates a Telegram OTP message in Messaggio.

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://msg.messaggio.com/api/v1`
- **Official documentation:** [Send Telegram OTP](https://messaggio.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipientPhone` | body | `string` | yes | Recipient phone number in international format without a plus sign. |
| `botToken` | body | `string` | yes | Telegram bot token configured as the sender code in Messaggio. |
| `otpCode` | body | `string` | yes | Telegram OTP code with 4 to 8 characters. Maximum length: 8. |
