# Reply to Comment with Superthread

## Endpoint

- **Method:** `POST`
- **Path:** `/:team_id/comments/:comment_id/children`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Reply to Comment](https://superthread.com/docs/api-docs/comments/reply-to-a-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `comment_id` | path | `string` | yes | Comment ID to reply to. |
| `content` | body | `string` | yes | Reply content. |
