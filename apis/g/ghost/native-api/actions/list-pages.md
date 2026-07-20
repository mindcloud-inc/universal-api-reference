# List Pages with Ghost

Retrieves pages from Ghost.

## Endpoint

- **Method:** `GET`
- **Path:** `/pages/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [List Pages](https://docs.ghost.org/admin-api/pages/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Comma-separated related resources to include. |
| `formats` | query | `string` | no | Comma-separated content formats to return. |
| `filter` | query | `string` | no | Ghost filter expression for narrowing pages. |
| `order` | query | `string` | no | Ghost order expression for sorting pages. |
