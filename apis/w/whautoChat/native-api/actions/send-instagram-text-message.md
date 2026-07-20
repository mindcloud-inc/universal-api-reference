# Send Instagram Text Message with WhautoChat

Sends an Instagram text message from WhautoChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/instagram/sendtext`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Send Instagram Text Message](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#7-send-instagram-text-message)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact.id` | body | `string` | no |
| `workspace.id` | body | `string` | no |
| `textMessage` | body | `string` | no |
| `scheduleDateTime` | body | `date` | no |
