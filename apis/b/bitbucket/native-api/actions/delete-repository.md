# Delete Repository with Bitbucket

Deletes a repository from Bitbucket.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/repositories/:workspace/:repo_slug`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [Delete Repository](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/#api-repositories-workspace-repo-slug-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace` | path | `string` | yes | Workspace slug that owns the repository. |
| `repo_slug` | path | `string` | yes | Repository slug to delete. |
