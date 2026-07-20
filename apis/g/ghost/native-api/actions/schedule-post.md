# Schedule Post with Ghost

Schedules a post in Ghost.

## Endpoint

- **Method:** `PUT`
- **Path:** `/posts/:id/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Schedule Post](https://docs.ghost.org/admin-api/posts/scheduling-a-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ghost post ID to schedule. |
| `posts[].updated_at` | body | `string` | yes | Current updated timestamp for optimistic locking. |
| `posts[].published_at` | body | `string` | yes | Future publish timestamp for the scheduled post. |
