# Create Or Replace Repository with DeployHQ

Creates or replaces the repository in DeployHQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/repository`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Create Or Replace Repository](https://api.deployhq.com/docs#tag/Repositories/operation/createProjectRepository)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `repository` | body | `object` | yes | Repository payload. DeployHQ accepts fields such as url, scm_type, protocol, username, password, branch, port, root_path, hosting_service_type, and manual_config. |
