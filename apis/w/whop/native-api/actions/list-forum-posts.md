# List Forum Posts with Whop

Retrieves forum posts from the Whop platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/forum_posts`
- **Base URL:** `https://api.whop.com`
- **Official documentation:** [List Forum Posts](https://docs.whop.com/api-reference/forum-posts/list-forum-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experience_id` | query | `string` | yes | The unique identifier of the experience to list forum posts for. |
