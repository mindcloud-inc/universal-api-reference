# Chat with AI with 1minAI

Creates an AI chat response in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/chat-with-ai`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Chat with AI](https://docs.1min.ai/docs/api/chat-with-ai-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `prompt` | body | `string` | yes |
| `conversationId` | body | `string` | no |
| `webSearch` | body | `boolean` | no |
