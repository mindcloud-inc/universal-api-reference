# Get Commit with Bitbucket

Retrieves a commit from Bitbucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/:workspace/:repo_slug/commit/:commit`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [Get Commit](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-commits/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commit` | path | `string` | no | Commit hash. |
| `repo_slug` | path | `string` | no | Repository slug. |
| `workspace` | path | `string` | no | Workspace slug. |
