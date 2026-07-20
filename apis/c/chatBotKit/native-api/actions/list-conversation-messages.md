# List Conversation Messages with ChatBotKit

## Endpoint

- **Method:** `GET`
- **Path:** `/conversation/{conversationId}/message/list`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [List Conversation Messages](https://chatbotkit.com/manuals/conversation-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | The ID of the conversation to list messages for |
| `cursor` | query | `string` | no | The cursor to use for pagination |
| `order` | query | `list` | no | The order of the paginated items Accepted values: `asc`, `desc`. |
| `take` | query | `number` | no | The number of items to retrieve |
