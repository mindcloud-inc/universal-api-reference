# List WhatsApp Templates with Mocean API

## Endpoint

- **Method:** `GET`
- **Path:** `/template/whatsapp/message_templates`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [List WhatsApp Templates](https://moceanapi.com/docs#get-all-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Optional template category filter. |
| `language` | query | `string` | no | Optional template language filter. |
| `limit` | query | `string` | no | Maximum number of templates to return. |
| `name` | query | `string` | no | Optional template name filter. |
| `status` | query | `string` | no | Optional template review status filter. |
