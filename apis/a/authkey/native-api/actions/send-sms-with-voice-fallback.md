# Send SMS With Voice Fallback with Authkey

Sends an SMS with voice fallback through Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.authkey.io/request`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Send SMS With Voice Fallback](https://authkey.io/sms-api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | Recipient country dialing code. |
| `fb1voice` | query | `string` | no | Fallback voice text if SMS delivery fails. |
| `mobile` | query | `string` | no | Recipient mobile number. |
| `sender` | query | `string` | no | Sender ID. |
| `sms` | query | `string` | no | SMS message content. |
