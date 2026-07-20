# Rate AI Answer with Chatling

Rates an AI answer in Chatling.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/chatbots/:chatbotId/conversations/:conversationId/messages/:messageId/rate-ai-answer`
- **Base URL:** `https://api.chatling.ai/v2`
- **Official documentation:** [Rate AI Answer](https://docs.chatling.ai/api-reference/v2/conversations/rate-ai-answer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatbotId` | path | `string` | yes | The chatbot ID. |
| `conversationId` | path | `string` | yes | The conversation ID. |
| `messageId` | path | `string` | yes | The message ID. |
| `rating` | body | `string` | yes | The rating to apply: 0 remove, 1 helpful, -1 not helpful. |
