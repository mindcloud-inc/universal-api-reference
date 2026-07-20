# Send SMS From Template (POST) with Authkey

Sends an SMS from a template in Authkey.

## Endpoint

- **Method:** `POST`
- **Path:** `https://console.authkey.io/restapi/requestjson.php`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Send SMS From Template (POST)](https://authkey.io/sms-api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | body | `string` | no | Recipient country dialing code. |
| `mobile` | body | `string` | no | Recipient mobile number. |
| `sid` | body | `string` | no | SMS template SID. |
