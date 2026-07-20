# Remove Conversation Tag with Front

Removes a tag from a conversation in Front.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/conversations/:conversation_id/tags`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [Remove Conversation Tag](https://dev.frontapp.com/reference/remove-conversation-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | The conversation ID. |
| `tag_ids[]` | body | `array<string>` | yes | Tag IDs to remove. |
