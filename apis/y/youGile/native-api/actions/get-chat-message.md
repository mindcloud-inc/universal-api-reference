# Get chat message with YouGile

Retrieves a chat message from YouGile.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats/:chatId/messages/:id`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [Get chat message](https://ru.yougile.com/api-v2#/operations/ChatMessageController_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The YouGile chat ID. |
| `id` | path | `number` | yes | The YouGile message ID. |
