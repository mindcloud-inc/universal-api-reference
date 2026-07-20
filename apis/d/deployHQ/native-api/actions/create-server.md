# Create Server with DeployHQ

Creates a new server in DeployHQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/servers`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Create Server](https://api.deployhq.com/docs#tag/Servers/operation/createProjectServer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `server` | body | `object` | yes | Server payload. DeployHQ accepts fields such as name, protocol_type, server_path, root_path, branch, environment, server_group_identifier, agent_id, and enabled. |
