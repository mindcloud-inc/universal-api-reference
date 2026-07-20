# Delete Server with DeployHQ

Deletes an existing server from DeployHQ.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/servers/:id`
- **Base URL:** `https://{account}.deployhq.com`
- **Official documentation:** [Delete Server](https://api.deployhq.com/docs#tag/Servers/operation/deleteProjectServer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The identifier or permalink of the project. |
| `id` | path | `string` | yes | The identifier of the server. |
