# Get Time Off Policy with Clockify

Retrieves a time off policy from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/time-off/policies/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Time Off Policy](https://docs.developer.clockify.me/#tag/Policy/operation/getPolicy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `id` | path | `string<string>` | yes |
