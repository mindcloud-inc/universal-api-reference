# Chat With Knowledge Base AI with Chatling

Chats with Chatling's knowledge base AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbots/:chatbotId/ai/kb/chat`
- **Base URL:** `https://api.chatling.ai/v2`
- **Official documentation:** [Chat With Knowledge Base AI](https://docs.chatling.ai/api-reference/v2/ai-kb/chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatbotId` | path | `string` | yes | The chatbot ID. |
| `message` | body | `string` | yes | The message to send to the AI. |
| `ai_model_id` | body | `number` | yes | The ID of the AI model to use for the response. |
| `conversation_id` | body | `string` | no | The conversation ID to continue. Leave blank to create a new conversation. |
| `contact_id` | body | `string` | no | The contact ID to associate with the conversation. |
| `language_id` | body | `number` | no | The ID of the language to use for the AI response. |
| `temperature` | body | `number` | no | The temperature to use for the AI response. |
| `instructions[]` | body | `array<string>` | no | Optional instruction strings to tailor the AI response. |
