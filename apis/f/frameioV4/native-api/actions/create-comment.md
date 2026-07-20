# Create Comment with Frame.io v4

Creates a new comment in Frame.io v4.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/files/:fileId/comments`
- **Base URL:** `https://api.frame.io/v4`
- **Official documentation:** [Create Comment](https://next.developer.frame.io/platform/api-reference/comments/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `file_id` | path | `string` | yes |
| `timestamp_as_timecode` | query | `boolean` | no |
| `data` | body | `object` | yes |
