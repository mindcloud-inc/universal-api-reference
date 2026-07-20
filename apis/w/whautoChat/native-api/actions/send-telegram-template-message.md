# Send Telegram Template Message with WhautoChat

Sends a Telegram template message from WhautoChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/telegram/sendtemplate`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Send Telegram Template Message](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/messages/#9-send-telegram-template-message)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact.id` | body | `string` | no |
| `workspace.id` | body | `string` | no |
| `buttons[]` | body | `array<string>` | no |
| `textMessage` | body | `string` | no |
