# Send Bulk SMS with WhatsBoost

Sends bulk SMS messages from WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/send/sms.bulk`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Send Bulk SMS](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mode` | body | `string` | yes | Mode of sending the message, it can be 'devices' which will allow you to use your linked android devices or 'credits' which will allow you to use gateways and partner devices. 'credits' requires you to have enough credit balance to send messages. |
| `campaign` | body | `string` | yes | Name of the campaign, you will see this in the SMS campaign manager. |
| `numbers` | body | `string` | no | List of phone numbers separated by commas. It can be optional if 'groups' parameter is not empty. It will accept E.164 formatted numbers or locally formatted numbers using the country code from your profile settings. E.164: +34612345678 Local: 612345678. |
| `groups` | body | `string` | no | List of contact group ID's separated by commas. It can be optional if 'numbers' parameter is not empty. You can get group ID's from /get/groups (Your contact groups). |
| `message` | body | `string` | yes | Message you want to send, spintax and shortcodes are supported. |
| `device` | body | `string` | no | Linked device unique ID, this is required if you will send with 'devices' mode. You can get linked device unique ID from /get/devices (Your devices). |
| `gateway` | body | `string` | no | Partner device unique ID or gateway ID, this is required if you will send with 'credits' mode. You can get a partner device unique ID and gateway ID from /get/rates. |
| `sim` | body | `number` | no | SIM slot number you want to use. For 'devices' mode only. |
| `priority` | body | `number` | no | Priority level. 0 or 1 = high priority (sent immediately), 2 = normal priority (queued). For 'devices' mode only. |
| `shortener` | body | `number` | no | Shortener ID, specify the shortener you want to use if you want to shorten the links in your message. You can get the list of available shorteners from /get/shorteners. |
