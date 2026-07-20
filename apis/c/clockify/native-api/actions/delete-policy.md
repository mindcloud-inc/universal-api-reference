# Delete Policy with Clockify

Deletes an existing policy from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/time-off/policies/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Policy](https://docs.developer.clockify.me/#tag/Policy/operation/deletePolicy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `id` | path | `string<string>` | yes |
