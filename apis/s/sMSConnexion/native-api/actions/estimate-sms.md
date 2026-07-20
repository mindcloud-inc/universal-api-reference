# Estimate SMS with SMS Connexion

Estimates a new SMS in SMS Connexion.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/estimate`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Estimate SMS](https://sms.cx/sms-api-documentation/#operation/EstimateSms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | Recipient phone number in E.164 format. |
| `from` | body | `string` | yes | Approved originator/sender ID. |
| `text` | body | `string` | yes | SMS message content. |
