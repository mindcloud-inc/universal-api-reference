# Send WhatsApp Custom Template Message with D7 Messaging

Sends a WhatsApp custom template message through D7 Messaging.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsapp/v2/send`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Send WhatsApp Custom Template Message](https://d7networks.com/docs/whatsapp/send-templated-message/custom-template-messages/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[].originator` | body | `string` | yes | Registered WhatsApp sender phone number. |
| `messages[].recipients[].recipient` | body | `string` | yes | Recipient mobile number in E.164 format including country code. |
| `messages[].content.template.template_id` | body | `string` | yes | Approved WhatsApp template identifier. |
| `messages[].content.template.language` | body | `string` | no | Language code configured for the template. |
| `messages[].report_url` | body | `string` | no | Webhook URL to receive delivery reports for this message. |
