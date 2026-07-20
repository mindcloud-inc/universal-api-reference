# Publish Post with Ghost

Publishes a draft post in Ghost.

## Endpoint

- **Method:** `PUT`
- **Path:** `/posts/:id/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Publish Post](https://docs.ghost.org/admin-api/posts/publishing-a-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ghost post ID to publish. |
| `posts[].updated_at` | body | `string` | yes | Current updated timestamp for optimistic locking. |
