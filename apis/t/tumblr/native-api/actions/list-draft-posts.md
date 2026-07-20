# List Draft Posts with Tumblr

Retrieves draft posts from a Tumblr blog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blog/:blogIdentifier/posts/draft`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [List Draft Posts](https://www.tumblr.com/docs/en/api/v2#postsdraft--retrieve-draft-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | Any Tumblr blog identifier for the target blog. |
| `before_id` | query | `string` | no | Return draft posts that appear before this post ID. |
| `filter` | query | `list<string>` | no | Format to return instead of default HTML output. Accepted values: `raw`, `text`. |
