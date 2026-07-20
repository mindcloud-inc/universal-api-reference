# Send Single SMS with WhatsBoost

Sends a single SMS from WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/send/sms`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Send Single SMS](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mode` | body | `string` | yes | Mode of sending the message, it can be 'devices' which will allow you to use your linked android devices or 'credits' which will allow you to use gateways and partner devices. 'credits' requires you to have enough credit balance to send messages. |
| `phone` | body | `string` | yes | Recipient mobile number, it will accept E.164 formatted numbers or locally formatted numbers using the country code from your profile settings. Example for Spain: E.164: +34612345678, Local: 612345678. |
| `message` | body | `string` | yes | Message you want to send, spintax is also supported. |
| `device` | body | `string` | no | Linked device unique ID, this is required if you will send with 'devices' mode. You can get linked device unique IDs from /get/devices (Your devices). |
| `gateway` | body | `string` | no | Partner device unique ID or gateway ID, this is required if you will send with 'credits' mode. You can get partner device unique ID and gateway ID from /get/rates. |
| `sim` | body | `number` | no | SIM slot number you want to use. For 'devices' mode only. |
| `priority` | body | `number` | no | Priority level. 0 or 1 = high priority (sent immediately), 2 = normal priority (queued). For 'devices' mode only. |
| `shortener` | body | `number` | no | Shortener ID, specify the shortener you want to use if you want to shorten the links in your message. You can get the list of available shorteners from /get/shorteners. |
