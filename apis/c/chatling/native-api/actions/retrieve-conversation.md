# Retrieve Conversation with Chatling

Retrieves a conversation from Chatling.

## Endpoint

- **Method:** `GET`
- **Path:** `/chatbots/:chatbotId/conversations/:conversationId`
- **Base URL:** `https://api.chatling.ai/v2`
- **Official documentation:** [Retrieve Conversation](https://docs.chatling.ai/api-reference/v2/conversations/retrieve-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatbotId` | path | `string` | yes | The chatbot ID. |
| `conversationId` | path | `string` | yes | The conversation ID. |
