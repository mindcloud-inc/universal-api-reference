# Get Workspace Member with Bitbucket

Retrieves a workspace member from Bitbucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspace/members/:member`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [Get Workspace Member](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-workspaces/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `member` | path | `string` | no | Workspace member identifier. |
| `workspace` | path | `string` | no | Workspace slug. |
