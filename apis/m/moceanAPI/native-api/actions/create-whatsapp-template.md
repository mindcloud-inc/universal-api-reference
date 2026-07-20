# Create WhatsApp Template with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/template/whatsapp/message_templates`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Create WhatsApp Template](https://moceanapi.com/docs#creating-whatsapp-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allowCategoryChange` | body | `string` | no | Allow Meta to reassign the category when needed. |
| `category` | body | `string` | yes | Template category. |
| `components` | body | `string` | yes | JSON array string describing template components. |
| `language` | body | `string` | yes | Template language code. |
| `message_send_ttl_seconds` | body | `string` | no | Optional authentication template TTL in seconds. |
| `name` | body | `string` | yes | Template name using lowercase letters, numbers, and underscores. |
