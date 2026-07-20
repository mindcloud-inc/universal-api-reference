# Get Project with Bitbucket

Retrieves a project from Bitbucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspace/projects/:project_key`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [Get Project](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-projects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_key` | path | `string` | no | Project key. |
| `workspace` | path | `string` | no | Workspace slug. |
