# Get User Workspace Permission with Bitbucket

Retrieves your workspace permission from Bitbucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/workspaces/:workspace/permission`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [Get User Workspace Permission](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace` | path | `string` | no | Workspace slug. |
