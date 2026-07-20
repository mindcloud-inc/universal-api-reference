# Get Comment with Frame.io v4

Retrieves a comment from Frame.io v4.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/comments/:commentId`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Get Comment](https://next.developer.frame.io/platform/api-reference/comments/show)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `comment_id` | path | `string` | yes |
| `timestamp_as_timecode` | query | `boolean` | no |
| `include` | query | `string` | no |
