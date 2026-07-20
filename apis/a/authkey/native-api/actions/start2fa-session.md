# Start 2FA Session with Authkey

Starts a 2FA session in Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.authkey.io/request`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Start 2FA Session](https://authkey.io/2fa-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mobile` | query | `string` | yes | Recipient mobile number for the OTP request. |
| `country_code` | query | `string` | yes | Recipient country dialing code. |
| `sid` | query | `string` | yes | Template SID for the OTP message. |
