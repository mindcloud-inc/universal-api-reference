# Send Messenger Media Message with WhautoChat

Sends a Messenger media message from WhautoChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/messenger/sendmedia`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Send Messenger Media Message](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#5-send-messenger-media-message)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact.id` | body | `string` | no |
| `workspace.id` | body | `string` | no |
| `mediaUrl` | body | `string` | no |
| `mimeType` | body | `string` | no |
| `scheduleDateTime` | body | `date` | no |
