# List Shared Library Users and Groups with Seafile

Retrieves users and groups a Seafile library is shared with.

## Endpoint

- **Method:** `GET`
- **Path:** `https://plus.seafile.com/api2/repos/{repoId}/dir/shared_items/`
- **Base URL:** `https://plus.seafile.com/api2`
- **Official documentation:** [List Shared Library Users and Groups](https://seafile-api.readme.io/reference/get_api2-repos-repo-id-dir-shared-items)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `repo_id` | path | `string` | no |
