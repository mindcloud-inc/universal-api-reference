# List Queued Posts with Tumblr

Retrieves queued posts from a Tumblr blog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blog/:blogIdentifier/posts/queue`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [List Queued Posts](https://www.tumblr.com/docs/en/api/v2#postsqueue--retrieve-queued-posts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | Any Tumblr blog identifier for the target blog. |
| `filter` | query | `list<string>` | no | Format to return instead of default HTML output. Accepted values: `raw`, `text`. |
