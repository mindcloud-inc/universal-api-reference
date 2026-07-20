# Update Workspace with Shuffll

Updates an existing workspace in Shuffll.

## Endpoint

- **Method:** `PUT`
- **Path:** `/auth/organization/:organizationId/workspace/:workspaceId`
- **Base URL:** `https://api.shuffll.com/api/v1`
- **Official documentation:** [Update Workspace](https://api-docs.shuffll.com/apis/workspaces/updateworkspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | New workspace name. |
| `organizationId` | path | `string` | yes | Shuffll organization id. |
| `workspaceId` | path | `string` | yes | Shuffll workspace id. |
