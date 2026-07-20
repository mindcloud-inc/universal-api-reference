# Send SMS (POST) with Authkey

Sends an SMS message through Authkey.

## Endpoint

- **Method:** `POST`
- **Path:** `https://console.authkey.io/restapi/requestjson.php`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Send SMS (POST)](https://authkey.io/sms-api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | body | `string` | no | Recipient country dialing code. |
| `mobile` | body | `string` | no | Recipient mobile number. |
| `pe_id` | body | `string` | no | DLT principal entity ID. |
| `sender` | body | `string` | no | Sender ID. |
| `template_id` | body | `string` | no | DLT template ID. |
