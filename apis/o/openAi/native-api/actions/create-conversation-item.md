# Create Conversation Item with Open AI

Creates items in a conversation in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/conversations/:conversation_id/items`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Create Conversation Item](https://developers.openai.com/api/reference/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID that will receive the item. |
| `items[]` | body | `array<object>` | yes | Items to append to the conversation. |
