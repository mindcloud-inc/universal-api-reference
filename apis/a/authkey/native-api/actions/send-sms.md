# Send SMS with Authkey

Sends an SMS message through Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.authkey.io/request`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Send SMS](https://authkey.io/sms-api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | Recipient country dialing code. |
| `mobile` | query | `string` | no | Recipient mobile number. |
| `pe_id` | query | `string` | no | DLT principal entity ID. |
| `sender` | query | `string` | no | Sender ID. |
| `sms` | query | `string` | no | SMS message content. |
| `template_id` | query | `string` | no | DLT template ID. |
