# List Conversation Messages with SeaX

Retrieves messages for a SeaX conversation.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations/{conversation_id}/messages`
- **Base URL:** `https://seax.seasalt.ai/seax-api/api/v1/workspace/{workspaceId}`
- **Official documentation:** [List Conversation Messages](https://api.seasalt.ai/seax/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation identifier. |
