# Send WhatsApp Text Message with D7 Networks

Sends a WhatsApp text message with D7 Networks.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsapp/v2/send`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Send WhatsApp Text Message](https://d7networks.com/docs/whatsapp/send-message/text-message/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[].originator` | body | `string` | yes | WhatsApp Business sender number or configured originator. |
| `messages[].recipients[].recipient` | body | `string` | yes | Recipient WhatsApp number with country code. |
| `messages[].content.text.body` | body | `string` | yes | Text body to send. |
| `messages[].content.text.preview_url` | body | `boolean` | no | Whether WhatsApp should render link previews. |
