# Update Server with DeployHQ

Updates an existing server in DeployHQ.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/servers/:id`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Update Server](https://api.deployhq.com/docs#tag/Servers/operation/updateProjectServer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `id` | path | `string` | yes | The identifier of the server. |
| `server` | body | `object` | yes | Server settings payload. DeployHQ accepts fields such as name, protocol_type, server_path, root_path, branch, environment, server_group_identifier, agent_id, and enabled. |
