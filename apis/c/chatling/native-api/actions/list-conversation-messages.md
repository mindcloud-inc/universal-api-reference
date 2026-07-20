# List Conversation Messages with Chatling

Retrieves conversation messages from Chatling.

## Endpoint

- **Method:** `GET`
- **Path:** `/chatbots/:chatbotId/conversations/:conversationId/messages`
- **Base URL:** `https://api.chatling.ai/v2`
- **Official documentation:** [List Conversation Messages](https://docs.chatling.ai/api-reference/v2/conversations/list-conversation-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatbotId` | path | `string` | yes | The chatbot ID. |
| `conversationId` | path | `string` | yes | The conversation ID. |
| `sort` | query | `string` | no | The sort order for the conversation messages list. |
