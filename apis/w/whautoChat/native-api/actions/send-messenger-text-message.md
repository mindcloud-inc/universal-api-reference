# Send Messenger Text Message with WhautoChat

Sends a Messenger text message from WhautoChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/messenger/sendtext`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Send Messenger Text Message](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#4-send-messenger-text-message)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact.id` | body | `string` | no |
| `workspace.id` | body | `string` | no |
| `textMessage` | body | `string` | no |
| `scheduleDateTime` | body | `date` | no |
