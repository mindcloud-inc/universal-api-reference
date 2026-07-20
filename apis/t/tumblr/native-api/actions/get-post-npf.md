# Get Post (NPF) with Tumblr

Retrieves a Tumblr post using NPF.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/blog/:blogIdentifier/posts/:postId`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Get Post (NPF)](https://www.tumblr.com/docs/en/api/v2#postspost-id---fetching-a-post-neue-post-format)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | Any blog identifier. |
| `postId` | path | `string` | yes | The post ID to fetch. |
