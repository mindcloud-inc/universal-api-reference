# Send Template Message with Growby

Sends a template message through Growby.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [Send Template Message](https://www.postman.com/growby/workspace/growby/folder/29609016-3d951c54-49db-4942-ae2c-f1e767b3736c)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | no | Approved WhatsApp sender number, for example 919016243183. |
| `language_code` | body | `string` | no | Template language code, for example en_US. |
| `password` | body | `string` | no | Growby password for the v1 messaging API. |
| `template_name` | body | `string` | no | Approved template name. |
| `to` | body | `string` | no | Recipient phone number with country code. |
| `type` | body | `string` | no | This action sends a template message. |
| `username` | body | `string` | no | Growby username for the v1 messaging API. |
