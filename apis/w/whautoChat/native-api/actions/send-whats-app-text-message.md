# Send WhatsApp Text Message with WhautoChat

Sends a WhatsApp text message from WhautoChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/whatsapp/sendtext`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Send WhatsApp Text Message](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#1-send-whatsapp-text-message)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact.id` | body | `string` | no |
| `workspace.id` | body | `string` | no |
| `textMessage` | body | `string` | no |
| `scheduleDateTime` | body | `date` | no |
