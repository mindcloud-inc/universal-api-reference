# Create Post with ContentStudio

Creates a new social media post in ContentStudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspace_id/posts`
- **Base URL:** `https://api.contentstudio.io/api/v1`
- **Official documentation:** [Create Post](https://api-prod.contentstudio.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accounts[]` | body | `array<string>` | yes | Account IDs to post to. |
| `approval` | body | `object` | no | Optional approval workflow payload. |
| `campaign_id` | body | `string` | no | Optional campaign ID. |
| `content` | body | `object` | yes | Post content payload. |
| `content_category_id` | body | `string` | no | Optional content category ID. |
| `first_comment` | body | `object` | no | Optional first comment payload. |
| `gmb_options` | body | `object` | no | Optional Google Business Profile options. |
| `labels[]` | body | `array<string>` | no | Optional label IDs. |
| `pinterest_options` | body | `object` | no | Optional Pinterest options. |
| `post_type` | body | `string` | no | Optional post type. |
| `post_video_title` | body | `string` | no | Optional video title. |
| `scheduling` | body | `object` | yes | Scheduling payload. |
| `tiktok_options` | body | `object` | no | Optional TikTok options. |
| `workspace_id` | path | `string` | yes | ContentStudio workspace ID. |
| `youtube_options` | body | `object` | no | Optional YouTube options. |
