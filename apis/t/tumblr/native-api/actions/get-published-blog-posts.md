# Get Published Blog Posts with Tumblr

Retrieves published posts from a Tumblr blog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blog/:blogIdentifier/posts`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Get Published Blog Posts](https://www.tumblr.com/docs/en/api/v2#posts--retrieve-published-posts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | Any blog identifier. |
| `type` | query | `list<string>` | no | Post type to return. Accepted values: `answer`, `audio`, `chat`, `link`, `photo`, `quote`, `text`, `video`. |
| `tag` | query | `string` | no | Limit the response to posts with the specified tag. |
| `id` | query | `string` | no | Return a specific post ID. |
| `reblog_info` | query | `boolean` | no | Return reblog information. |
| `notes_info` | query | `boolean` | no | Return note count and note metadata. |
| `filter` | query | `list<string>` | no | Alternative post format to return. Accepted values: `raw`, `text`. |
| `before` | query | `number` | no | Return posts published before this Unix timestamp in seconds. |
| `after` | query | `number` | no | Return posts published after this Unix timestamp in seconds. |
| `sort` | query | `list<string>` | no | Sort order for the returned posts. Accepted values: `asc`, `desc`. |
