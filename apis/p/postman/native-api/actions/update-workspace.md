# Update Workspace with Postman

Updates an existing workspace in Postman.

## Endpoint

- **Method:** `PUT`
- **Path:** `/workspaces/:workspaceId`
- **Base URL:** `https://api.getpostman.com`
- **Official documentation:** [Update Workspace](https://www.postman.com/postman/free-public-apis/request/rkjj42d/update-a-workspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The workspace's ID. |
| `workspace.name` | body | `string` | no | — |
