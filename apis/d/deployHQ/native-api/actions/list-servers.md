# List Servers with DeployHQ

Retrieves all servers for a project from DeployHQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/servers`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [List Servers](https://api.deployhq.com/docs#tag/Servers/operation/listProjectServers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
