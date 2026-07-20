# List Workspace Policies with Clockify

Lists all workspace policies in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/time-off/policies`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Workspace Policies](https://docs.developer.clockify.me/#tag/Policy/operation/findPoliciesForWorkspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `name` | query | `string` | no | — |
| `status` | query | `list<string>` | no | Accepted values: `ACTIVE`, `ALL`, `ARCHIVED`. |
