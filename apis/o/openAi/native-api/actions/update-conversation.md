# Update Conversation with Open AI

Updates a conversation in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/conversations/:conversation_id`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Update Conversation](https://developers.openai.com/api/reference/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID to update. |
| `metadata` | body | `object` | no | Metadata to store on the conversation. |
