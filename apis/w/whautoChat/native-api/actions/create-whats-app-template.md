# Create WhatsApp Template with WhautoChat

Creates a new WhatsApp template in WhautoChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/whatsapp-template`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Create WhatsApp Template](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/whatsapp-templates/#3-create-whatsapp-template)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `template.category` | body | `string` | no |
| `template.language` | body | `string` | no |
| `template.name` | body | `string` | no |
| `template.components[]` | body | `array<object>` | no |
| `workspace.id` | body | `string` | no |
