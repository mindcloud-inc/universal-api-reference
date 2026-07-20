# Reblog Post (NPF) with Tumblr

Reblogs a Tumblr post using NPF.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/blog/:blogIdentifier/posts`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Reblog Post (NPF)](https://www.tumblr.com/docs/en/api/v2#posts---createreblog-a-post-neue-post-format)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | Any Tumblr blog identifier for the target blog. |
| `parent_tumblelog_uuid` | body | `string` | yes | UUID of the blog being reblogged from. |
| `parent_post_id` | body | `string` | yes | ID of the post being reblogged. |
| `reblog_key` | body | `string` | yes | Reblog key validating the reblog action. |
| `content[]` | body | `array<object>` | no | Optional NPF content blocks to add to the end of the reblog trail. |
| `state` | body | `list<string>` | no | Initial state for the new reblog post. Accepted values: `draft`, `private`, `published`, `queue`, `unapproved`. |
| `tags` | body | `string` | no | Comma-separated list of tags to associate with the reblog. |
| `layout[]` | body | `array<object>` | no | Optional NPF layout objects for arranging added content blocks. |
| `hide_trail` | body | `boolean` | no | Whether to hide the full reblog trail in the new reblog. |
| `exclude_trail_items[]` | body | `array<number>` | no | Specific reblog trail item indexes to exclude from the new reblog. |
| `publish_on` | body | `date` | no | Future ISO 8601 date/time to publish a queued reblog. |
| `date` | body | `date` | no | Past ISO 8601 date/time used to backdate the reblog. |
| `slug` | body | `string` | no | Custom URL slug to use in the reblog permalink. |
| `source_url` | body | `string` | no | Source attribution URL for the reblog content. |
| `interactability_reblog` | body | `list<string>` | no | Who can interact with this reblog when reblogging. Accepted values: `everyone`, `noone`. |
| `send_to_twitter` | body | `boolean` | no | Whether to share the reblog to a connected Twitter account. |
| `is_private` | body | `boolean` | no | Whether this should be a private answer when reblogging an answer post. |
