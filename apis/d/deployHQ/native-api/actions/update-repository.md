# Update Repository with DeployHQ

Updates the repository for a project in DeployHQ.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/repository`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Update Repository](https://api.deployhq.com/docs#tag/Repositories/operation/updateProjectRepository)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `repository` | body | `object` | yes | Repository settings payload. DeployHQ accepts fields such as url, scm_type, protocol, username, password, branch, port, root_path, hosting_service_type, and manual_config. |
