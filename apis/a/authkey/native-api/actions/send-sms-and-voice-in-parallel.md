# Send SMS And Voice In Parallel with Authkey

Sends SMS and voice messages in parallel through Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.authkey.io/request`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Send SMS And Voice In Parallel](https://authkey.io/sms-api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mobile` | query | `string` | yes | Recipient mobile number. |
| `country_code` | query | `string` | yes | Recipient country dialing code. |
| `sms` | query | `string` | yes | SMS message content. |
| `sender` | query | `string` | yes | Sender ID for the SMS request. |
| `voice` | query | `string` | yes | Voice message text to read during the call. |
