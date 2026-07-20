# List Message Templates with Growby

Retrieves message templates from Growby.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/messages_templates`
- **Base URL:** `https://api.growby.net`
- **Official documentation:** [List Message Templates](https://www.postman.com/growby/workspace/growby/folder/29609016-ef13f103-ac66-4520-8ca0-5ec329e30d00)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_token` | query | `string` | no | Meta Cloud API access token with WhatsApp permissions. |
| `email` | query | `string` | no | Email address associated with the WABA setup. |
| `phone_number_id` | query | `string` | no | Meta phone number ID for the linked WhatsApp sender. |
| `whatsapp_business_account_id` | query | `string` | no | WhatsApp Business Account ID. |
