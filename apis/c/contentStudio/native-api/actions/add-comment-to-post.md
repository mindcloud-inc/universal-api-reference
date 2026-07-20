# Add Comment to Post with ContentStudio

Adds a comment or internal note to a ContentStudio post.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspace_id/posts/:post_id/comments`
- **Base URL:** `https://api.contentstudio.io/api/v1`
- **Official documentation:** [Add Comment to Post](https://api-prod.contentstudio.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment` | body | `string` | yes | Comment text. |
| `is_note` | body | `boolean` | no | True to save an internal note. |
| `mentioned_users[]` | body | `array<string>` | no | User IDs to mention. |
| `post_id` | path | `string` | yes | ContentStudio post ID. |
| `workspace_id` | path | `string` | yes | ContentStudio workspace ID. |
