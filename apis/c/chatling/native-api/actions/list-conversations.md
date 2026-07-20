# List Conversations with Chatling

Retrieves conversations from Chatling.

## Endpoint

- **Method:** `GET`
- **Path:** `/chatbots/:chatbotId/conversations`
- **Base URL:** `https://api.chatling.ai/v2`
- **Official documentation:** [List Conversations](https://docs.chatling.ai/api-reference/v2/conversations/list-conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatbotId` | path | `string` | yes | The chatbot ID. |
| `sort` | query | `string` | no | The sort order for the conversations list. |
