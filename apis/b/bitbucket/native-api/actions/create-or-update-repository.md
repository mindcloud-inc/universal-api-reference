# Create Or Update Repository with Bitbucket

Creates or updates a repository in Bitbucket.

## Endpoint

- **Method:** `PUT`
- **Path:** `/repositories/:workspace/:repo_slug`
- **Base URL:** `https://api.bitbucket.org/2.0`
- **Official documentation:** [Create Or Update Repository](https://developer.atlassian.com/cloud/bitbucket/rest/api-group-repositories/#api-repositories-workspace-repo-slug-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace` | path | `string` | yes | Workspace slug that owns the repository. |
| `repo_slug` | path | `string` | yes | Repository slug to create or update. |
| `name` | body | `string` | yes | Human-readable repository name. |
| `description` | body | `string` | no | Repository description. |
| `is_private` | body | `boolean` | no | Whether the repository should be private. |
| `project.key` | body | `string` | no | Bitbucket project key for the repository. |
