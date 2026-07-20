# Get Library Commit Info with Seafile

Retrieves details for a Seafile library commit.

## Endpoint

- **Method:** `GET`
- **Path:** `https://plus.seafile.com/api/v2.1/repos/{repoId}/commits/{commitId}/`
- **Base URL:** `https://plus.seafile.com/api2`
- **Official documentation:** [Get Library Commit Info](https://seafile-api.readme.io/reference/get_api-v2-1-repos-repo-id-commits-commit-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `commit_id` | path | `string` | no |
| `repo_id` | path | `string` | no |
