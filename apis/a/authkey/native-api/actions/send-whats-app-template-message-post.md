# Send WhatsApp Template Message (POST) with Authkey

Sends a WhatsApp template message through Authkey.

## Endpoint

- **Method:** `POST`
- **Path:** `https://console.authkey.io/restapi/requestjson.php`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Send WhatsApp Template Message (POST)](https://authkey.io/whatsapp-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bodyValues.var1` | body | `string` | no | First template variable value. |
| `bodyValues.var2` | body | `string` | no | Second template variable value. |
| `country_code` | body | `string` | no | Recipient country dialing code. |
| `mobile` | body | `string` | no | Recipient mobile number. |
| `wid` | body | `string` | no | WhatsApp template ID. |
