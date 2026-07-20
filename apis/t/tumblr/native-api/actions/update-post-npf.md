# Update Post (NPF) with Tumblr

Updates an existing Tumblr post using NPF.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/blog/:blogIdentifier/posts/:postId`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Update Post (NPF)](https://www.tumblr.com/docs/en/api/v2#postspost-id---editing-a-post-neue-post-format)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | Any Tumblr blog identifier for the target blog. |
| `postId` | path | `string` | yes | ID of the post to edit. |
| `content[]` | body | `array<object>` | no | NPF content blocks for the edited post. |
| `state` | body | `list<string>` | no | Updated state for the post. Accepted values: `draft`, `private`, `published`, `queue`, `unapproved`. |
| `tags` | body | `string` | no | Comma-separated list of tags to associate with the post. |
| `layout[]` | body | `array<object>` | no | Optional NPF layout objects for arranging the content blocks. |
| `publish_on` | body | `date` | no | Future ISO 8601 date/time to publish a queued post. |
| `date` | body | `date` | no | Past ISO 8601 date/time used to backdate the post. |
| `slug` | body | `string` | no | Custom URL slug to use in the post permalink. |
| `source_url` | body | `string` | no | Source attribution URL for the post content. |
| `interactability_reblog` | body | `list<string>` | no | Who can interact with this post when reblogging. Accepted values: `everyone`, `noone`. |
| `send_to_twitter` | body | `boolean` | no | Whether to share the edited post to a connected Twitter account. |
| `is_private` | body | `boolean` | no | Whether this should be a private answer when editing an answer post. |
| `parent_tumblelog_uuid` | body | `string` | no | UUID of the reblog source blog when editing a reblog. |
| `parent_post_id` | body | `string` | no | ID of the reblog source post when editing a reblog. |
| `reblog_key` | body | `string` | no | Reblog key for the reblog source post when editing a reblog. |
| `hide_trail` | body | `boolean` | no | Whether to hide the full reblog trail in the edited reblog. |
| `exclude_trail_items[]` | body | `array<number>` | no | Specific reblog trail item indexes to exclude when editing a reblog. |
