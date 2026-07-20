# Get Post by ID with Ghost

Retrieves a post from Ghost by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/:id/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Get Post by ID](https://docs.ghost.org/admin-api/posts/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ghost post ID to retrieve. |
| `include` | query | `string` | no | Comma-separated related resources to include. |
| `formats` | query | `string` | no | Comma-separated content formats to return. |
