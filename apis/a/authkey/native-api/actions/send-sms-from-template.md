# Send SMS From Template with Authkey

Sends an SMS from a template in Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.authkey.io/request`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Send SMS From Template](https://authkey.io/sms-api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | Recipient country dialing code. |
| `mobile` | query | `string` | no | Recipient mobile number. |
| `sid` | query | `string` | no | SMS template SID. |
