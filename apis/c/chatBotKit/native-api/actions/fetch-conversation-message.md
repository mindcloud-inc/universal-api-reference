# Fetch Conversation Message with ChatBotKit

## Endpoint

- **Method:** `GET`
- **Path:** `/conversation/{conversationId}/message/{messageId}/fetch`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Fetch Conversation Message](https://chatbotkit.com/manuals/conversation-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | The ID of the conversation containing the message |
| `messageId` | path | `string` | yes | The ID of the message to retrieve |
