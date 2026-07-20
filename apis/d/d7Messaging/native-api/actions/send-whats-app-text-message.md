# Send WhatsApp Text Message with D7 Messaging

Sends a WhatsApp text message through D7 Messaging.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsapp/v2/send`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Send WhatsApp Text Message](https://d7networks.com/docs/whatsapp/send-message/text-message/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[].originator` | body | `string` | yes | Registered WhatsApp sender phone number. |
| `messages[].recipients[].recipient` | body | `string` | yes | Recipient mobile number in E.164 format including country code. |
| `messages[].content.text.body` | body | `string` | yes | Text message body. |
| `messages[].content.text.preview_url` | body | `boolean` | no | Whether URLs in the message body should generate previews. |
| `messages[].report_url` | body | `string` | no | Webhook URL to receive delivery reports for this message. |
