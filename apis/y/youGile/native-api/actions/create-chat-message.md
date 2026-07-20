# Create chat message with YouGile

Creates a chat message in YouGile.

## Endpoint

- **Method:** `POST`
- **Path:** `/chats/:chatId/messages`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [Create chat message](https://ru.yougile.com/api-v2#/operations/ChatMessageController_sendMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The YouGile chat ID. |
| `text` | body | `string` | yes | The plain-text message body. |
| `textHtml` | body | `string` | yes | The HTML-formatted message body. |
| `label` | body | `string` | yes | The message label. |
