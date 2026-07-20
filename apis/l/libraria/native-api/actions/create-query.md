# Create Query with Libraria

Make queries to a specific chatbot or library.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/library/:library_id/query`
- **Base URL:** `https://api.libraria.ai`
- **Official documentation:** [Create Query](https://docs.libraria.ai/api-reference/library-v2/create-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `library_id` | path | `string` | yes | The ID of the library you are going to ask a question. |
| `query` | body | `string` | yes | The question you will make to the library. |
| `conversationId` | body | `string` | no | Optional. Use this for a continuation of the conversation. |
