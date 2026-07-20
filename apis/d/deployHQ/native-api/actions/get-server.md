# Get Server with DeployHQ

Retrieves a server from DeployHQ.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/servers/:id`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Get Server](https://api.deployhq.com/docs#tag/Servers/operation/getProjectServerById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `id` | path | `string` | yes | The identifier of the server. |
