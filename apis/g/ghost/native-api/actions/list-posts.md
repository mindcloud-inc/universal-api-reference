# List Posts with Ghost

Retrieves posts from Ghost.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [List Posts](https://docs.ghost.org/admin-api/posts/overview)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Comma-separated related resources to include. |
| `formats` | query | `string` | no | Comma-separated content formats to return. |
| `filter` | query | `string` | no | Ghost filter expression for narrowing posts. |
| `order` | query | `string` | no | Ghost order expression for sorting posts. |
