# Update Conversation with Frameshift

Updates an existing conversation in Frameshift.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/projects/:project_id/conversations/:conversation_id`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Update Conversation](https://mosaic.frameshift.io/api/#api-Collections-UpdateConversation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `conversation_id` | path | `number` | yes |
| `title` | body | `string` | no |
| `description` | body | `string` | no |
