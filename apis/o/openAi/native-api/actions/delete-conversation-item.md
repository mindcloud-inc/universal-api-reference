# Delete Conversation Item with Open AI

Deletes an item from a conversation in Open AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v1/conversations/:conversation_id/items/:item_id`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Delete Conversation Item](https://developers.openai.com/api/reference/conversations/delete-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID that owns the item. |
| `item_id` | path | `string` | yes | Conversation item ID to delete. |
