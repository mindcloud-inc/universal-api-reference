# Get File History with Seafile

Retrieves the version history for a file in Seafile.

## Endpoint

- **Method:** `GET`
- **Path:** `https://plus.seafile.com/api/v2.1/repos/{repoId}/file/history/`
- **Base URL:** `https://plus.seafile.com/api2`
- **Official documentation:** [Get File History](https://seafile-api.readme.io/reference/get_api-v2-1-repos-repo-id-file-history)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `p` | query | `string` | no |
| `repo_id` | path | `string` | no |
