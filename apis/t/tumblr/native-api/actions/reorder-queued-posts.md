# Reorder Queued Posts with Tumblr

Reorders queued posts in a Tumblr blog.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/blog/:blogIdentifier/posts/queue/reorder`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Reorder Queued Posts](https://www.tumblr.com/docs/en/api/v2#postsqueuereorder--reorder-queued-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | Any Tumblr blog identifier for the target blog. |
| `post_id` | body | `string` | yes | ID of the queued post to move. |
| `insert_after` | body | `string` | no | Queued post ID to move the post after, or 0 to move it to the top. |
