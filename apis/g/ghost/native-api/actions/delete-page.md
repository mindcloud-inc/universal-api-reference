# Delete Page with Ghost

Deletes an existing page from Ghost.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/pages/:id/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Delete Page](https://docs.ghost.org/admin-api/pages/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ghost page ID to delete. |
