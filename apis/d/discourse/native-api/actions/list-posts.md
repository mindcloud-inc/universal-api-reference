# List Posts with Discourse

Retrieves latest posts across Discourse topics.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [List Posts](https://docs.discourse.org/#tag/Posts/operation/listPosts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | Only return posts with an ID lower than this value. |
