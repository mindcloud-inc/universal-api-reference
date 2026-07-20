# Create Query (Legacy) with Libraria

Given a query and an optional conversation ID, get a response from your library.

## Endpoint

- **Method:** `POST`
- **Path:** `/library/:library_id/query`
- **Base URL:** `https://api.libraria.ai`
- **Official documentation:** [Create Query (Legacy)](https://docs.libraria.ai/api-reference/library/create-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `library_id` | path | `string` | yes | The ID of the library you are going to ask a question. |
| `query` | body | `string` | yes | The question you will make to the library. |
| `conversationId` | body | `string` | no | Optional. Use this for a continuation of the conversation. |
