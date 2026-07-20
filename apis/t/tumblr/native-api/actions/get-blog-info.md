# Get Blog Info with Tumblr

Retrieves information for a Tumblr blog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blog/:blogIdentifier/info`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Get Blog Info](https://www.tumblr.com/docs/en/api/v2#info---retrieve-blog-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | Any blog identifier. |
| `fields[blogs]` | query | `string` | no | Comma-separated blog fields for a partial response. |
