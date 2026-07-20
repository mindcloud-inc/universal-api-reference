# Get Conversation Item with Open AI

Retrieves an item from a conversation in Open AI.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/conversations/:conversation_id/items/:item_id`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Get Conversation Item](https://developers.openai.com/api/reference/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID that owns the item. |
| `item_id` | path | `string` | yes | Conversation item ID to retrieve. |
