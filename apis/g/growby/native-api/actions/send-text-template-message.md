# Send Text Template Message with Growby

Sends a text template message through Growby.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/messages`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [Send Text Template Message](https://www.postman.com/growby-documentation/growby-api/request/u5iw6ai/send-text-template-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | no | Linked WhatsApp sender number. |
| `message_template.components` | body | `string` | no | JSON array of template component objects matching Growby's v3 template docs. |
| `message_template.langcode` | body | `string` | no | Template language code, for example en_US. |
| `message_template.name` | body | `string` | no | Approved WhatsApp template name. |
| `show_in_inbox` | body | `string` | no | Whether to show the message in the Growby inbox. |
| `to` | body | `string` | no | Recipient phone number with country code. |
