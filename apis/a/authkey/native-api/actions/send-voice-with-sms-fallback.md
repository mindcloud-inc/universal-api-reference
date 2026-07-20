# Send Voice With SMS Fallback with Authkey

Sends a voice call with SMS fallback through Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.authkey.io/request`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Send Voice With SMS Fallback](https://authkey.io/voice-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mobile` | query | `string` | yes | Recipient mobile number. |
| `country_code` | query | `string` | yes | Recipient country dialing code. |
| `voice` | query | `string` | yes | Voice message text to read during the call. |
| `sender` | query | `string` | yes | Sender ID for the fallback SMS request. |
| `fb1sms` | query | `string` | yes | Fallback SMS content if the voice call fails. |
