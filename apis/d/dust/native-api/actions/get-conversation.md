# Get Conversation with Dust

Retrieves a conversation from Dust by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/w/:workspaceId/assistant/conversations/:conversationId`
- **Base URL:** `https://dust.tt`
- **Official documentation:** [Get Conversation](https://docs.dust.tt/reference/get_api-v1-w-wid-assistant-conversations-cid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | Dust conversation sId. |
