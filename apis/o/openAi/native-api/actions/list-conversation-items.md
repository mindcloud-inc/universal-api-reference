# List Conversation Items with Open AI

Retrieves items from a conversation in Open AI.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/conversations/:conversation_id/items`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [List Conversation Items](https://developers.openai.com/api/reference/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID to list items for. |
