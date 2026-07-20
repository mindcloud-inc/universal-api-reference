# Get Page by ID with Ghost

Retrieves a page from Ghost by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/pages/:id/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Get Page by ID](https://docs.ghost.org/admin-api/pages/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ghost page ID to fetch. |
| `include` | query | `string` | no | Comma-separated related resources to include. |
| `formats` | query | `string` | no | Comma-separated content formats to return. |
