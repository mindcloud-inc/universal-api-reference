# Add Conversation Tag with Front

Adds a tag to a conversation in Front.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:conversation_id/tags`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [Add Conversation Tag](https://dev.frontapp.com/reference/add-conversation-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | The conversation ID. |
| `tag_ids[]` | body | `array<string>` | yes | Tag IDs to add. |
