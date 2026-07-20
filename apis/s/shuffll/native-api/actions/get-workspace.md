# Get Workspace with Shuffll

Retrieves a workspace from Shuffll by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/auth/organization/:organizationId/workspace/:workspaceId`
- **Base URL:** `https://api.shuffll.com/api/v1`
- **Official documentation:** [Get Workspace](https://api-docs.shuffll.com/apis/workspaces/getworkspacebyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Shuffll organization id. |
| `workspaceId` | path | `string` | yes | Shuffll workspace id. |
