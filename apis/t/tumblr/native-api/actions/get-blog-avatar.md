# Get Blog Avatar with Tumblr

Retrieves a Tumblr blog avatar by size.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blog/:blogIdentifier/avatar/:size`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Get Blog Avatar](https://www.tumblr.com/docs/en/api/v2#avatar--retrieve-a-blog-avatar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | Any blog identifier. |
| `size` | path | `list<number>` | yes | Avatar size in pixels. Accepted values: `128`, `16`, `24`, `30`, `40`, `48`, `512`, `64`, `96`. |
