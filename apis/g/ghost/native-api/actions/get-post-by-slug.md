# Get Post by Slug with Ghost

Retrieves a post from Ghost by slug.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/slug/:slug/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Get Post by Slug](https://docs.ghost.org/admin-api/posts/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Ghost post slug to retrieve. |
| `include` | query | `string` | no | Comma-separated related resources to include. |
| `formats` | query | `string` | no | Comma-separated content formats to return. |
