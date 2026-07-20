# Send Messenger Template Message with WhautoChat

Sends a Messenger template message from WhautoChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/messenger/sendtemplate`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Send Messenger Template Message](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#6-send-messenger-template-message)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact.id` | body | `string` | no |
| `workspace.id` | body | `string` | no |
| `elements[]` | body | `array<object>` | no |
