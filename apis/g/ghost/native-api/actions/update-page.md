# Update Page with Ghost

Updates an existing page in Ghost.

## Endpoint

- **Method:** `PUT`
- **Path:** `/pages/:id/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Update Page](https://docs.ghost.org/admin-api/pages/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ghost page ID to update. |
| `pages[].updated_at` | body | `string` | yes | Current updated_at value required by Ghost optimistic locking. |
| `pages[].title` | body | `string` | no | Updated page title. |
| `pages[].lexical` | body | `string` | no | Updated lexical editor JSON content. |
| `pages[].html` | body | `string` | no | Updated HTML content. |
