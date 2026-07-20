# Send International SMS with Authkey

Sends an international SMS through Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.authkey.io/request`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Send International SMS](https://authkey.io/sms-api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mobile` | query | `string` | yes | Recipient mobile number. |
| `country_code` | query | `string` | yes | Recipient country dialing code. |
| `sms` | query | `string` | yes | SMS message content. |
| `sender` | query | `string` | yes | Sender ID for the SMS request. |
