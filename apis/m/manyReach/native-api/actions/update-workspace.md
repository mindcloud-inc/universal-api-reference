# Update Workspace with ManyReach

Updates an existing workspace in ManyReach.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.manyreach.com/api/v2/workspaces/:id`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Update Workspace](https://api.manyreach.com/api#v2/tag/workspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Workspace ID. |
| `title` | body | `string` | no | Updated workspace title. |
