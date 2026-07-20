# Create Comment with Frameshift

Creates a comment in a Frameshift conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects/:project_id/conversations/:conversation_id/comments`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [Create Comment](https://mosaic.frameshift.io/api/#api-Collections-PostComment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `conversation_id` | path | `number` | yes |
| `text` | body | `string` | yes |
