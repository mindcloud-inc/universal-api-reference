# Create Post with Ghost

Creates a new post in Ghost.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Create Post](https://docs.ghost.org/admin-api/posts/creating-a-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `posts[].title` | body | `string` | yes | Title for the new post. |
| `posts[].status` | body | `string` | no | Initial status for the new post. |
| `posts[].lexical` | body | `string` | no | Ghost Lexical editor payload. |
| `posts[].html` | body | `string` | no | HTML content for the new post when source=html. |
| `source` | query | `string` | no | Input format for the content payload. |
