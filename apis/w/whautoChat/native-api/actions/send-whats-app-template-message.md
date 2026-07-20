# Send WhatsApp Template Message with WhautoChat

Sends a WhatsApp template message from WhautoChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/whatsapp/sendtemplate`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Send WhatsApp Template Message](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#3-send-whatsapp-template-message)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact.id` | body | `string` | no |
| `workspace.id` | body | `string` | no |
| `template` | body | `string` | no |
