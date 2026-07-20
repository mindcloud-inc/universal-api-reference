# Copy Page with Ghost

Creates a copy of a page in Ghost.

## Endpoint

- **Method:** `POST`
- **Path:** `/pages/:id/copy`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Copy Page](https://docs.ghost.org/admin-api/pages/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ghost page ID to copy. |
