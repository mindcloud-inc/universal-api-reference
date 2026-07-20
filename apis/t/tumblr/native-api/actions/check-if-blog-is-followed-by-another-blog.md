# Check If Blog Is Followed By Another Blog with Tumblr

Checks whether a Tumblr blog is followed by another blog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blog/:blogIdentifier/followed_by`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Check If Blog Is Followed By Another Blog](https://www.tumblr.com/docs/en/api/v2#followed_by--check-if-followed-by-blog)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | The blog that may be followed by another blog. |
| `query` | query | `string` | yes | The name of the blog that may be following your blog. |
