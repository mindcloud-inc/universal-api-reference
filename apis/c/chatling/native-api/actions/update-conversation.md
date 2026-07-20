# Update Conversation with Chatling

Updates an existing conversation in Chatling.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/chatbots/:chatbotId/conversations/:conversationId`
- **Base URL:** `https://api.chatling.ai/v2`
- **Official documentation:** [Update Conversation](https://docs.chatling.ai/api-reference/v2/conversations/update-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatbotId` | path | `string` | yes | The chatbot ID. |
| `conversationId` | path | `string` | yes | The conversation ID. |
| `archive` | body | `boolean` | no | Whether to archive the conversation. |
| `important` | body | `boolean` | no | Whether to mark the conversation as important. |
| `contact_id` | body | `string` | no | The contact ID to associate with the conversation. |
