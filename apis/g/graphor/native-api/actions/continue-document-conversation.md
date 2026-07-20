# Continue Document Conversation with Graphor

Retrieves follow-up answers from Graphor with conversation memory.

## Endpoint

- **Method:** `POST`
- **Path:** `/ask-sources`
- **Base URL:** `https://sources.graphorlm.com`
- **Official documentation:** [Continue Document Conversation](https://docs.graphorlm.com/api-reference/chat-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | body | `string` | yes | Conversation identifier returned by a previous chat response. |
| `question` | body | `string` | yes | The follow-up question to ask. |
