# Send SMS Verification with FraudLabs Pro

Sends an SMS verification in FraudLabs Pro.

## Endpoint

- **Method:** `POST`
- **Path:** `v2/verification/send`
- **Base URL:** `https://api.fraudlabspro.com/`
- **Official documentation:** [Send SMS Verification](https://www.fraudlabspro.com/developer/api/send-sms-verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tel` | body | `string` | yes | The recipient mobile phone number in E164 format. |
| `mesg` | body | `string` | yes | The SMS template including the <otp> placeholder. |
