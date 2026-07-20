# Update Comment with Frame.io v4

Updates an existing comment in Frame.io v4.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts/:accountId/comments/:commentId`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Update Comment](https://next.developer.frame.io/platform/api-reference/comments/update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `comment_id` | path | `string` | yes |
| `timestamp_as_timecode` | query | `boolean` | no |
| `data` | body | `object` | yes |
