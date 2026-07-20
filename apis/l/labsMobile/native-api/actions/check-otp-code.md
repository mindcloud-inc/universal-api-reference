# Check OTP Code with LabsMobile

Checks the status of an OTP code in LabsMobile.

## Endpoint

- **Method:** `GET`
- **Path:** `/otp/checkCode`
- **Base URL:** `https://api.labsmobile.com`
- **Official documentation:** [Check OTP Code](https://www.labsmobile.com/en/sms-api/api-versions/sms-otp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `env` | query | `string` | no | OTP environment name. |
| `phone_number` | query | `string` | yes | Phone number to check. |
