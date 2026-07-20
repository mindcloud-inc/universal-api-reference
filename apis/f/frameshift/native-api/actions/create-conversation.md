# Create Conversation with Frameshift

Creates a new conversation in Frameshift.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:project_id/conversations`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Create Conversation](https://mosaic.frameshift.io/api/#api-Collections-CreateConversation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `title` | body | `string` | yes |
| `description` | body | `string` | no |
