# Create Broadcast with AWeber

Creates a new broadcast in AWeber.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/lists/:listId/broadcasts`
- **Base URL:** `https://api.aweber.com/1.0`
- **Official documentation:** [Create Broadcast](https://api.aweber.com/#tag/Broadcasts/paths/~1accounts~1{accountId}~1lists~1{listId}~1broadcasts/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `body_amp` | body | `string` | no |
| `body_html` | body | `string` | yes |
| `body_text` | body | `string` | yes |
| `click_tracking_enabled` | body | `boolean` | no |
| `exclude_lists` | body | `string` | no |
| `facebook_integration` | body | `string` | no |
| `include_lists` | body | `string` | no |
| `is_archived` | body | `boolean` | no |
| `listId` | path | `string` | yes |
| `notify_on_send` | body | `boolean` | no |
| `segment_link` | body | `string` | no |
| `subject` | body | `string` | yes |
| `twitter_integration` | body | `string` | no |
