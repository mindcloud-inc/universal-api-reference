# List Workspace Templates with Shuffll

Retrieves workspace templates from Shuffll.

## Endpoint

- **Method:** `GET`
- **Path:** `/auth/organization/:organizationId/workspace/:workspaceId/templates`
- **Base URL:** `https://api.shuffll.com/api/v1`
- **Official documentation:** [List Workspace Templates](https://api-docs.shuffll.com/apis/templates/gettemplatesbyorgworkspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Shuffll organization id. |
| `workspaceId` | path | `string` | yes | Shuffll workspace id. |
