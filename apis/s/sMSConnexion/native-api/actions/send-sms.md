# Send SMS with SMS Connexion

Sends an SMS message with SMS Connexion.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Send SMS](https://sms.cx/sms-api-documentation/#operation/SendSms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | Recipient phone number in E.164 format. |
| `from` | body | `string` | yes | Approved originator/sender ID. |
| `text` | body | `string` | yes | SMS message content. |
