# Send OTP Code with LabsMobile

Creates and sends an OTP code with LabsMobile.

## Endpoint

- **Method:** `GET`
- **Path:** `/otp/sendCode`
- **Base URL:** `https://api.labsmobile.com`
- **Official documentation:** [Send OTP Code](https://www.labsmobile.com/en/sms-api/api-versions/sms-otp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `digits` | query | `string` | no | Number of digits in the OTP code. |
| `env` | query | `string` | no | OTP environment name. |
| `message` | query | `string` | no | SMS message template containing %CODE%. |
| `phone_number` | query | `string` | yes | Destination phone number in E.164 format. |
| `sender` | query | `string` | no | Sender name for the OTP message. |
| `test` | query | `string` | no | Use simulated send mode. |
