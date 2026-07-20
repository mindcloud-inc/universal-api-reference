# Delete Conversation Message with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/conversation/{conversationId}/message/{messageId}/delete`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Delete Conversation Message](https://chatbotkit.com/manuals/conversation-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | The ID of the conversation |
| `messageId` | path | `string` | yes | The ID of the message to delete |
