# Send WhatsApp Media Template with Authkey

Sends a WhatsApp media template through Authkey.

## Endpoint

- **Method:** `GET`
- **Path:** `https://console.authkey.io/restapi/request.php`
- **Base URL:** `https://console.authkey.io/restapi`
- **Official documentation:** [Send WhatsApp Media Template](https://authkey.io/whatsapp-api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | query | `string` | no | Recipient country dialing code. |
| `HeaderData` | query | `string` | no | Public file URL for the media header. |
| `headerFileName` | query | `string` | no | Header file name. |
| `mobile` | query | `string` | no | Recipient mobile number. |
| `wid` | query | `string` | no | WhatsApp template ID. |
