# Send Instagram Template Message with WhautoChat

Sends an Instagram template message from WhautoChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/instagram/sendtemplate`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Send Instagram Template Message](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#8-send-instagram-template-message)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact.id` | body | `string` | no |
| `workspace.id` | body | `string` | no |
| `elements[]` | body | `array<object>` | no |
