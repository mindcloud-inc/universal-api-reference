# Send OTP with WhatsBoost

Sends a one-time password from WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/send/otp`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Send OTP](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Type of message, it can be SMS or WhatsApp. |
| `message` | body | `string` | yes | OTP message to send, you can use {{otp}} shortcode to include the OTP anywhere in the message. |
| `phone` | body | `string` | yes | Recipient mobile number, it will accept E.164 formatted numbers. Example for Spain: E.164: +34612345678. |
| `expire` | body | `number` | no | OTP expiration time in seconds. Default value is 300 seconds or 5 minutes. |
| `priority` | body | `number` | no | For WhatsApp only. If you want to send the message as priority, it will be sent immediately. 1 for yes and 2 for no. |
| `account` | body | `string` | no | This is only for WhatsApp type. WhatsApp account you want to use for sending, you can get account unique IDs from /get/wa.accounts or in the dashboard. |
| `mode` | body | `string` | no | This is only required for SMS type. This is the mode of sending the message. 'devices' allows you to use linked Android devices, while 'credits' uses gateways and requires sufficient credit balance. |
| `device` | body | `string` | no | This is only for SMS type. Linked device unique ID, required for 'devices' mode. You can get linked device unique IDs from /get/devices (Your devices). |
| `gateway` | body | `string` | no | This is only for SMS type. Partner device unique ID or gateway ID, required for 'credits' mode. You can get partner device and gateway IDs from /get/rates. |
| `sim` | body | `number` | no | This is only for SMS type. SIM slot number you want to use, for 'devices' mode only. |
