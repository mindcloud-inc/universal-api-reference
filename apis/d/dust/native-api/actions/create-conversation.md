# Create Conversation with Dust

Creates a new conversation in Dust.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/w/:workspaceId/assistant/conversations`
- **Base URL:** `https://dust.tt`
- **Official documentation:** [Create Conversation](https://docs.dust.tt/reference/post_api-v1-w-wid-assistant-conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Conversation title. |
