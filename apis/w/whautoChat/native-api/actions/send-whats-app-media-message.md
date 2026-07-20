# Send WhatsApp Media Message with WhautoChat

Sends a WhatsApp media message from WhautoChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/whatsapp/sendmedia`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Send WhatsApp Media Message](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#2-send-whatsapp-media-message)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact.id` | body | `string` | no |
| `workspace.id` | body | `string` | no |
| `mediaUrl` | body | `string` | no |
| `mimeType` | body | `string` | no |
| `scheduleDateTime` | body | `date` | no |
