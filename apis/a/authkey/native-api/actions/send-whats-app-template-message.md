# Send WhatsApp Template Message with Authkey

Sends a WhatsApp template message through Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://console.authkey.io/restapi/request.php`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Send WhatsApp Template Message](https://authkey.io/whatsapp-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | Recipient country dialing code. |
| `mobile` | query | `string` | no | Recipient mobile number. |
| `wid` | query | `string` | no | WhatsApp template ID. |
