# List Replies to a Comment with Superthread

## Endpoint

- **Method:** `GET`
- **Path:** `/:team_id/comments/:comment_id/children`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [List Replies to a Comment](https://superthread.com/docs/api-docs/comments/get-replies)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `team_id` | path | `string` | yes |
| `comment_id` | path | `string` | yes |
