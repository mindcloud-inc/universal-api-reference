# Send Voice Call From Template with Authkey

Sends a templated voice call through Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.authkey.io/request`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Send Voice Call From Template](https://authkey.io/voice-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | Recipient country dialing code. |
| `mobile` | query | `string` | no | Recipient mobile number. |
| `vid` | query | `string` | no | Voice template ID. |
