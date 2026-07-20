# Get Post Notes with Tumblr

Retrieves notes for a Tumblr post.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blog/:blogIdentifier/notes`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Get Post Notes](https://www.tumblr.com/docs/en/api/v2#notes---get-notes-for-a-specific-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | Any blog identifier. |
| `id` | query | `string` | yes | The post ID to fetch notes for. |
| `before_timestamp` | query | `number` | no | Fetch notes created before this Unix timestamp in seconds. |
| `mode` | query | `list<string>` | no | Response formatting mode for the returned notes. Accepted values: `all`, `conversation`, `likes`, `reblogs_with_tags`, `rollup`. |
