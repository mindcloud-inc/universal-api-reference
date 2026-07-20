# Get WhatsApp Template Variables with Zixflow

Retrieves WhatsApp template variables from Zixflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaign/whatsapp/variable-keys`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Get WhatsApp Template Variables](https://docs.zixflow.com/api-reference/campaign/whatsapp/template-variable-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneId` | query | `string` | yes | WhatsApp sender phone identifier from Zixflow WhatsApp Settings. |
| `templateName` | query | `string` | yes | WhatsApp template name, for example welcome_message. |
| `language` | query | `string` | yes | Template language code, for example en. |
