# Update Post with Ghost

Updates an existing post in Ghost.

## Endpoint

- **Method:** `PUT`
- **Path:** `/posts/:id/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Update Post](https://docs.ghost.org/admin-api/posts/updating-a-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ghost post ID to update. |
| `posts[].updated_at` | body | `string` | yes | Current updated timestamp for optimistic locking. |
| `posts[].title` | body | `string` | no | Updated post title. |
| `posts[].lexical` | body | `string` | no | Updated Ghost Lexical editor payload. |
| `posts[].html` | body | `string` | no | Updated HTML content when source=html. |
| `source` | query | `string` | no | Input format for the content payload. |
| `save_revision` | query | `string` | no | Whether Ghost should store a revision for this update. |
