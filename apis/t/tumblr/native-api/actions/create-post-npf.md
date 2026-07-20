# Create Post (NPF) with Tumblr

Creates a new Tumblr post using NPF.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/blog/:blogIdentifier/posts`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Create Post (NPF)](https://www.tumblr.com/docs/en/api/v2#posts---createreblog-a-post-neue-post-format)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | Any Tumblr blog identifier for the target blog. |
| `content[]` | body | `array<object>` | yes | NPF content blocks to include in the post. |
| `state` | body | `list<string>` | no | Initial state for the new post. Accepted values: `draft`, `private`, `published`, `queue`, `unapproved`. |
| `tags` | body | `string` | no | Comma-separated list of tags to associate with the post. |
| `layout[]` | body | `array<object>` | no | Optional NPF layout objects for arranging the content blocks. |
| `publish_on` | body | `date` | no | Future ISO 8601 date/time to publish a queued post. |
| `date` | body | `date` | no | Past ISO 8601 date/time used to backdate the post. |
| `slug` | body | `string` | no | Custom URL slug to use in the post permalink. |
| `source_url` | body | `string` | no | Source attribution URL for the post content. |
| `interactability_reblog` | body | `list<string>` | no | Who can interact with this post when reblogging. Accepted values: `everyone`, `noone`. |
| `send_to_twitter` | body | `boolean` | no | Whether to share the post to a connected Twitter account. |
| `is_private` | body | `boolean` | no | Whether this should be a private answer when creating an answer post. |
