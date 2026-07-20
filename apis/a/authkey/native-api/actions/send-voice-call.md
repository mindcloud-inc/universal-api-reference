# Send Voice Call with Authkey

Sends a voice call through Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.authkey.io/request`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Send Voice Call](https://authkey.io/voice-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mobile` | query | `string` | yes | Recipient mobile number for the voice call. |
| `country_code` | query | `string` | yes | Recipient country dialing code. |
| `voice` | query | `string` | yes | Voice message text to read during the call. |
