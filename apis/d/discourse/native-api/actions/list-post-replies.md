# List Post Replies with Discourse

Retrieves replies to a Discourse post.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/:id/replies.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [List Post Replies](https://docs.discourse.org/#tag/Posts/operation/postReplies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Numeric Discourse post ID. |
