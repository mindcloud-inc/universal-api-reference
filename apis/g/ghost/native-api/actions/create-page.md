# Create Page with Ghost

Creates a new page in Ghost.

## Endpoint

- **Method:** `POST`
- **Path:** `/pages/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Create Page](https://docs.ghost.org/admin-api/pages/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pages[].title` | body | `string` | yes | Title for the new Ghost page. |
| `pages[].status` | body | `string` | no | Initial status for the page. |
| `pages[].lexical` | body | `string` | no | Lexical editor JSON content for the page. |
| `pages[].html` | body | `string` | no | HTML content for the page. |
| `source` | query | `string` | no | Optional source format for the create payload. |
