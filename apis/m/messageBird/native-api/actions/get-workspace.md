# Get Workspace with MessageBird

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/workspaces/:workspaceId`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Get Workspace](https://docs.bird.com/api/accounts-api/api-reference/organizations/workspaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | The Bird organization ID that owns the workspace. |
| `workspaceId` | path | `string` | yes | The Bird workspace ID you want to retrieve. |
