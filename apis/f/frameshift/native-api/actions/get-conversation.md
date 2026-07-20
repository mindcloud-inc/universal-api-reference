# Get Conversation with Frameshift

Retrieves detailed conversation information from Frameshift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/conversations/:conversation_id`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Get Conversation](https://mosaic.frameshift.io/api/#api-Project_Conversations-GetConversation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `conversation_id` | path | `number` | yes |
