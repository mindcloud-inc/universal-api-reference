# Delete Post with Ghost

Deletes an existing post from Ghost.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/posts/:id/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Delete Post](https://docs.ghost.org/admin-api/posts/deleting-a-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ghost post ID to delete. |
